# Hi there, I'm Cooper!

[![Github Stats](https://github-readme-stats.vercel.app/api?username=noonels&count_private=true&show_icons=true)](https://github.com/noonels)

```go
cooper := About {
     Summary: "Endlessly curious, endlessly eager to tell you about it",
     WorkingOn: "Teaching myself the ins and outs of Scientific Computing -- mostly using Fortran and Julia",
     LookingToCollaborate: true,
     Contact: &ContactInfo {
         Github: "github.com/noonels",
         LinkedIn: "linkedin.com/in/cooper-healy-a6140718a/",
         Email: "m.cooper.healy@gmail.com",
     }
}

type ContactInfo struct {
    GitHub   string
    LinkedIn string
    Email    string
}
 
type About struct {
    Summary              string
    WorkingOn            string
    LookingToCollaborate bool
    Contact              *ContactInfo
}
```
