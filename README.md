# AI Defense in Prod: Minimal and Zero CVE CUDA Images with Chainguard

## DESCRIPTION
Deep learning is moving out of the lab and into production at a breakneck pace. However, as CNNs get baked into real-time applications and models run in inference become the responsibility of devops teams, security becomes a major issue.

In this presentation, Dr. Patrick Smyth, Staff Developer Relations Engineer at Chainguard, will discuss and demo new CUDA-powered Chainguard Images. While runtime images for major AI frameworks tend to throw in the kitchen sink by including hundreds of packages, these Chainguard Images for PyTorch and NeMo aim to be as minimal as possible to reduce attack surface, and at time of writing have 0 CVEs compared to the dozens of CVEs in official images. We'll train a simple animal recognition model, compare these images with their official counterparts, and discuss some of the advantages and tradeoffs in building on these base images. And, yes, there will be some jokes and animated GIFs along the way

## SPEAKER
### Patrick Smith
- Staff Developer Relations Engineer at Chainguard
- born and raised in Queens
- Researcher at Columbia University
- PhD in Digital Humanity from Columbia
- Space Telescope Science Institute
- [https://twitter.com/@psmyth01](https://twitter.com/@psmyth01)
- [https://www.linkedin.com/in/smythp/](https://www.linkedin.com/in/smythp/)

## LINKS
- [https://www.chainguard.dev/unchained/announcing-early-access-to-chainguards-cuda-optimized-images](https://www.chainguard.dev/unchained/announcing-early-access-to-chainguards-cuda-optimized-images)
- [https://go.chainguard.dev/pytorch-intro](https://go.chainguard.dev/pytorch-intro)
- [https://github.com/docker/scout-cli](https://github.com/docker/scout-cli)
- [https://huggingface.co/docs/transformers/en/index](https://huggingface.co/docs/transformers/en/index)
- [https://edu.chainguard.dev/chainguard/chainguard-images/getting-started/pytorch-cuda](https://edu.chainguard.dev/chainguard/chainguard-images/getting-started/pytorch-cuda)

## COMMANDS
```bash
docker pull --platform linux/x86_64 cgr.dev/chainguard/pytorch-cuda12:latest-dev

trivy nvcr.io/nvidia/nemo:24.03.01.framework
```

Running grype command on an image:
```bash
grype <image name and tag>
```

Running docker scout command:
```bash
docker scout cves nvcr.io/nvidia/nemo:24.03.01.framework
```
