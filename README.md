# Lab8 report

First we need to build our image using following command:

```bash
docker buildx build -q -f Dockerfile_classic -t monio359/lab8:v1 --sbom=true --provenance=mode=max --push .
```

Using the command below, we can now determine whether the image contains any vulnerabilities.

```bash
docker scout quickview monio359/lab8:v
```

![](./previews/scout_quickview.png)

What catches attention are 4 critical vulnerabilities and 10 high ones. Now I will present how to eliminate these vulnerabilities