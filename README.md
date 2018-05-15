# cgo
A test binary that uses cgo

# Equinox Test

```
$ equinox release --version 0.0.2 --app app_doi6qTkaTpA --signing-key=equinox.key --platforms="darwin_amd64"
----> Looking for an existing release with version 0.0.2..., done
      No release with version 0.0.2 found
----> Checking for channel stable..., done
----> Building for each target platform in parallel
      Successfully built target for darwin_amd64
      sha256  89c63674d2113627a237f5b69bb3187bea088bdc7f41bcdd0a5d1e4379c9357d
      sig     306402303ac44ceca1d426bf4f89032e0839fdd0df5e936f79a6a1f9ce73c2c0
              b7c5ab9f5773b67e6e065ed45f37ba209d841c5002306da40e130be55fd0a911
              5900bcfe9e0a01bd5578aea0c29abebaab3dde5ccdf0d7fa3638b27186a8ebac
              77c305c20de7
----> Creating a release..., version 0.0.2
----> Uploading assets...
      Uploading binary for darwin_amd64
----> Publishing release..., done

Release version 0.0.2 uploaded. It will be published to the stable channel after
package builds complete. Your downloads will be available at:

  https://dl.equinox.io/equinox/cgo/stable

$ CGO_ENABLED=0 equinox release --version 0.0.3 --app app_doi6qTkaTpA --signing-key=equinox.key --platforms="darwin_amd64"
----> Looking for an existing release with version 0.0.3..., done
      No release with version 0.0.3 found
----> Checking for channel stable..., done
----> Building for each target platform in parallel
      Failed building target for darwin_amd64

Build directory: /var/folders/pl/8z9yxvdj3_93w3pgx670wjf80000gn/T/equinox-605574819

can't load package: package github.com/kyleconroy/cgo: build constraints exclude all Go files in /Users/kyle/go/src/github.com/kyleconroy/cgo

The build for platform darwin_amd64 failed with the above error message. The
release was not published to Equinox.
```
