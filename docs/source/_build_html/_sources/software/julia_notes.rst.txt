julia notes
===========


Using kwargs...
-----------------

function:
::

  function test(A; kwargs...)

      kw = Dict(kwargs)

      # if there was nothing passed -> set default
      if !haskey(kw,:mode); kw = Dict(:mode => :default) end
      mode = get(kw, :mode, 0);

      if mode == :default
        B = 10
      elseif mode == :LGRM
        B = A
      else
        print("pick a mode","\n")
      end
      return B
  end

  B=test(2)
  B=test(2;(:mode=>:LGRM))
