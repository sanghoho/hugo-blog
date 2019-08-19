---
title: "Sample Tag"
date: 2019-08-13T22:37:18+09:00
draft: false
categories: ["data-science"]
subcategories: ["visualization"]
tags: ["python3", "test", "tutorial"]
cover: ""
---

{{< highlight go "linenos=table,hl_lines=8 15-17,linenostart=199" >}}
// GetTitleFunc returns a func that can be used to transform a string to
// title case.
//
// The supported styles are
//
// - "Go" (strings.Title)
// - "AP" (see https://www.apstylebook.com/)
// - "Chicago" (see https://www.chicagomanualofstyle.org/home.html)
//
// If an unknown or empty style is provided, AP style is what you get.
func GetTitleFunc(style string) func(s string) string {
  switch strings.ToLower(style) {
  case "go":
    return strings.Title
  case "chicago":
    tc := transform.NewTitleConverter(transform.ChicagoStyle)
    return tc.Title
  default:
    tc := transform.NewTitleConverter(transform.APStyle)
    return tc.Title
  }
}

{{< / highlight >}}

- `python3`

{{<highlight python "linenos=table">}}

from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello World!'

def say_hello(name):
    print("Hello {}!".foramt(name))

if __name__ == '__main__':
    app.run(port=4895)  

{{</highlight>}}
