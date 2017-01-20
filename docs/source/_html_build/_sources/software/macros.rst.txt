Macros
======

Detailed information on macros in julia is found `here <http://docs.julialang.org/en/release-0.5/manual/metaprogramming/>`_.

@def
----
Given some parameters:
::

  using Parameters

  @with_kw immutable Vpara @deftype Float64
      m  = 2.6887e+03
  end
  pa = Vpara(); # initialize parameter set


Instead of unpackaging the same parameters each time in a nested function like this:
::

  function outer_f(pa::Vpara)
    num = zeros(Float64, (10,1))
    for i in 1:10
     num[i] = inner_f(pa::Vpara,i)
    end
    return num
  end

with:
::

  function inner_f(pa::Vpara,i)
    @unpack_Vpara pa
     m + i + 0.1
  end

We define a macro as:
::

  macro def(name, definition)
    return quote
      macro $name()
        esc($(Expr(:quote, definition)))
      end
    end
  end

then redefine ``inner_f1()`` as:
::

  @def inner_f2 begin
    m + i + 0.1
  end

We also need to modify the ``outer_f()`` as:
::

  function outer_f(pa::Vpara)
    @unpack_Vpara pa
    num = zeros(Float64, (10,1))
    for i in 1:10
      num[i] = @inner_f2
    end
    return num
  end

The ``@def`` macro is functionally equivalent to copying and pasting the contents of inner_f() into outer_f().
