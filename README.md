#Example of `method_missing` and `Rake::TestTask`
##SYNOPSIS

    require "html"

    q= HTML.new {  
      html {
        head { title "My wonderful home page" }
        body do
          h1 "Welcome to my home page!"
          b "My hobbies:"
          ul do
            li "Juggling"
            li "Knitting"
            li { i "Sleeping" } 
            li "Metaprogramming"
          end #ul
        end # body
      }
    }

`q.to_s` produces:

        <html>
        <head>
        <title>
        My wonderful home page
        </title>
        </head><body>
        <h1>
        Welcome to my home page!
        </h1><b>
        My hobbies:
        </b><ul>
        <li>
        Juggling
        </li><li>
        Knitting
        </li><li>
        <i>
        Sleeping
        </i>
        </li><li>
        Metaprogramming
        </li>
        </ul>
        </body>
        </html>
