# SLSA workflow examples

In this repository you can find some examples on how to secure your software supply chain by implementing [SLSA](https://slsa.dev) requirements.

To do so I make use of the following tools:

- [GitHub action][github-actions]
- [Sigstore][sigstore]
- [Syft][syft]
- [in-toto][in-toto]
- [SLSA Provenance][slsa-provenance]
- [SLSA requirements][slsa-requirements]
- [SLSA Provenance Action][slsa-provenance-action]

See the [workflows](.github/workflows) on how to utilize these tools to secure your own software supply chains. 

## Go App

To compile the Go app you can simply run the following command.

```bash
go build -o bin/slsa-workflow-example .
```

Or simply build the Docker image.

```bash
docker build -t ghcr.io/marcofranssen/slsa-workflow-example .
```

[slsa-workflow-example]: https://github.com/marcofranssen/slsa-workflow-example "SLSA GitHub actions workflow example"
[slsa-provenance-action]: https://github.com/philips-labs/slsa-provenance-action "SLSA provenance action"
[slsa-provenance]: https://slsa.dev/provenance "SLSA provenance specification"
[slsa-requirements]: https://slsa.dev/spec/v0.1/requirements "SLSA requirements required to meet SLSA levels"
[in-toto]: https://in-toto.io/ "A framework to secure the integrity of software supply chains"
[syft]: https://github.com/anchore/syft "A CLI tool and Go library for generating a Software Bill of Materials (SBOM) from container images and filesystems."
[sigstore]: https://www.sigstore.dev/ "A new standard for signing, verifying and protecting software"
[github-actions]: https://docs.github.com/en/actions "Automate, customize, and execute your software development workflows right in your repository with GitHub Actions."


## #External References

https://github.com/marketplace/actions/docker-metadata-action

https://docs.docker.com/build/ci/github-actions/manage-tags-labels/

https://github.com/slsa-framework/slsa-github-generator/blob/main/internal/builders/container/README.md

https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-to-the-container-registry

https://marcofranssen.nl/oci-as-attestations-storage-for-your-packages

https://marcofranssen.nl/secure-your-software-supply-chain-using-sigstore-and-github-actions
