---
title: "TIL Blog"
date: 2021-05-26T17:37:59+02:00
draft: false
---

initial post just for testing

{{< highlight go "linenos=table,hl_lines=8 15-17,linenostart=199" >}}
func GetTitleFunc(style string) func(s string) string {
  switch strings.ToLower(style) {
  case "go":
    return strings.Title
  case "chicago":
    return transform.NewTitleConverter(transform.ChicagoStyle)
  default:
    return transform.NewTitleConverter(transform.APStyle)
  }
}
{{< / highlight >}}