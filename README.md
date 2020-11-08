# Summary

Containerised development environment for my machine learning studying. Built primarily to develop code in python.

## Prerequisites

Install the following on the host and client.

* Host
  * Docker
  * Git
* Client
  * Docker
  * Visual Studio Code
    * Remote - Containers extension
  * Git

## Steps

1. Ensure Docker is running on the host.
2. (If using remote host) set up a Docker context on the client which will connect to the host.
    * Example:

    ```json
    {
        "Name": "helios",
        "Metadata": {},
        "Endpoints": {
            "docker": {
                "Host": "ssh://zcauchi@helios64.local",
                "SkipTLSVerify": false
            }
        },
        "TLSMaterial": {},
        "Storage": {
            "MetadataPath": "C:\\Users\\zachc\\.docker\\contexts\\meta\\48582bd628b7c80064780ba9ecce2d435db042b40bd4335a7cea4b4c254e8178",
            "TLSPath": "C:\\Users\\zachc\\.docker\\contexts\\tls\\48582bd628b7c80064780ba9ecce2d435db042b40bd4335a7cea4b4c254e8178"
        }
    }
    ```

3. Open the Run Task dialog (`F1` or `Ctrl + Shift + P`) and select Remote-Containers: Clone Repository in Container Volume.
4. Enter in Git clone URL and select destination volume.
5. Once process completes, env should be completely set up.
