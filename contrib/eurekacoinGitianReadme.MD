## Set env var

```

export SIGNER=Bago213
export VERSION=0.17.5

```

## linux

```

sudo bitstash/contrib/gitian-build-linux.py ${SIGNER} ${VERSION} --build --docker -j3

sudo ./bin/gsign --signer ${SIGNER} --release ${VERSION}-linux-unsigned --destination ../gitian.sigs/ ../bitstash/contrib/gitian-descriptors/gitian-linux.yml

./bin/gverify -v -d ../gitian.sigs/ -r ${VERSION}-linux-unsigned ../bitstash/contrib/gitian-descriptors/gitian-linux.yml


```

## windows

```

sudo bitstash/contrib/gitian-build-windows.py ${SIGNER} ${VERSION} --build --docker -j3

sudo ./bin/gsign --signer ${SIGNER} --release ${VERSION}-windows-unsigned --destination ../gitian.sigs/ ../bitstash/contrib/gitian-descriptors/gitian-windows.yml

./bin/gverify -v -d ../gitian.sigs/ -r ${VERSION}-windows-unsigned ../bitstash/contrib/gitian-descriptors/gitian-windows.yml

```

## mac

```

sudo bitstash/contrib/gitian-build-osx.py ${SIGNER} ${VERSION} --build --docker -j3

sudo ./bin/gsign --signer ${SIGNER} --release ${VERSION}-osx-unsigned --destination ../gitian.sigs/ ../bitstash/contrib/gitian-descriptors/gitian-osx.yml

./bin/gverify -v -d ../gitian.sigs/ -r ${VERSION}-osx-unsigned ../bitstash/contrib/gitian-descriptors/gitian-osx.yml


```


