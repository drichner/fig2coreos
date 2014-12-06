Fig2coreos in docker container!
==============================

Fig2coreos is useful to generate service files from fig.yml files

Read more about [Fig2coreos][1] 



How to run?
-----------

Default `docker run drichner/fig2coreos` shows fig2coreos help information.

To run fig please specify fig.yml directory:
```
docker run -v $(pwd):/config -it drichner/fig2coreos --help
```


Helper script, just create fig2coreos file somewhere in path and copy this snippet:

    #!/bin/bash
    docker run -it -v $(pwd):/config drichner/fig2coreos "$@"

then you can execute ```fig2coreos  testapp fig.yml coreos-service/```


  [1]: https://github.com/CenturyLinkLabs/fig2coreos