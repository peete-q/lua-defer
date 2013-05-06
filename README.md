lua-defer
=========

A lua 5.x distribution with defer semantic support, like golang

##example

    function foo()
        defer
            print 'defer 1'
        end
    
        do
            defer print 'defer 2' end
        end
    
        defer print 'defer 3' end

        print 'end'
    end

###output

    defer 2
    end
    defer 3
    defer 1

    
