# multiplication works

    Code
      s <- html_session("http://hadley.nz")
    Code
      s
    Output
      <session> http://hadley.nz
        Status: 200
        Type:   text/html
        Size:   9090
    Code
      s <- jump_to(s, "hadley-wickham.jpg")
    Code
      session_history(s)
    Output
        http://hadley.nz
      - http://hadley.nz/hadley-wickham.jpg
    Code
      s <- back(s)
    Code
      s <- follow_link(s, 2)
    Message <message>
      Navigating to #page-top
    Code
      session_history(s)
    Output
        http://hadley.nz
      - http://hadley.nz#page-top
