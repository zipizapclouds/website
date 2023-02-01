---
author: dholbach
date: 2023-02-20 12:30:00+00:00
title: February 2023 Update
description: "XX"
url: /blog/2023/03/february-2023-update/
tags: [monthly-update]
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
---

As the Flux family of projects and its communities are growing, we
strive to inform you each month about what has already landed, new
possibilities which are available for integration, and where you can get
involved. Read our last update [here](/blog/2023/02/january-2023-update/).

It's the beginning of March 2023 - let's recap together what
happened in March - it has been a lot!

## News in the Flux family

### Next Flux release: more stability and performance improvements

We have released [Flux v0.39](https://github.com/fluxcd/flux2/releases/tag/v0.39.0).
Users are encouraged to upgrade for the best experience.

Highlights

- Starting with this version, the Flux controllers come with [SBOMs and
  SLSA Provenance Attestations](/flux/security/)
  embedded in their container images.
- The [Flux Terraform Provider](https://github.com/fluxcd/terraform-provider-flux)
  has a new resource for bootstrapping Flux, without depending on
  third-party Terraform providers, that allows customising the
  controllers at install time. Users are encouraged to migrate to
  this new resource and provide feedback.
- The Flux CLI is now included in [Wolfi OS](https://github.com/wolfi-dev/os),
  the Linux (Un)distro designed for securing the software supply chain. The
  Chainguard team and Wolfi maintainers are shipping updates for the Flux
  package on a regular basis.

Features and improvements

- Recreate immutable resources (e.g. Kubernetes Jobs) by annotating
  or labeling them with `kustomize.toolkit.fluxcd.io/force: enabled`.
- Support for HTTPS bearer token authentication for Git repositories.
- Improve memory usage by disabling the caching of `Secret` and
  `ConfigMap` resources in all controllers.
- Better observability with progressive status updates for Sources
  (Git, OCI, Helm, S3 Buckets).
- Allow extracting the OCI artifact SHA256 digest for Cosign with
  `flux push artifact -o json`.
- Track CRDs managed by Flux, `flux trace` and `flux tree` will show
  which HelmRelease deployed which CRDs.
- Allow the Flux GitHub Action to use a GitHub token when checking
  for updates to avoid rate limiting.

Documentation

- Security: [Software Bill of Materials](/flux/security/#software-bill-of-materials)
- Security: [SLSA Provenance Attestations](/flux/security/#slsa-provenance-attestations)
- Security: [Scanning Flux images for CVEs](/flux/security/#scanning-for-cves)

Big thanks to all the Flux contributors that helped us with this release!

### Security news

We extended our [Security Docs](/flux/security/) to show more examples for
verifying SBOMs. Now the newly introduced SLSA Provenance Attestation
feature is documented as well.

### Flagger x.y.z

### Flux Ecosystem

<!--

If you add entries to this subsection, please don't use "we" as it gets
confusing from which perspective the whole blog post is written and who
"we" is. The whole post is meant to be from the perspective of the Flux
community. Better to write:]

- "Since the new release of X, it supports Y." or
- "Team lead X says: 'we have put a lot of effort into Y and are
   really proud of the performance results' ..." or
- "The team has been working on ..."

-->

#### Flux Subsystem for Argo

#### Terraform-controller

#### Weave GitOps

- <https://github.com/weaveworks/weave-gitops/releases/tag/v0.17.0>
- <https://github.com/weaveworks/weave-gitops/releases/tag/v0.16.0>

#### Azure GitOps

#### VS Code GitOps Extension

#### New additions to the Flux Ecosystem

## Recent & Upcoming Events

It's important to keep you up to date with new features and developments
in Flux and provide simple ways to see our work in action and chat with
our engineers.

### Recent Events (ICYMI) 📺

We feel blessed to have such a big community of users, contributors and
integrators and so many are happy to talk about their experiences. In
February here are a couple of talks we would like to highlight.

Here is a list of additional videos and topics we really enjoyed -
please let us know if we missed anything of interest and we will make
sure to mention it in the next post!

### Upcoming Events 📆

We are happy to announce that we have a number of events coming up in
March - tune in to learn more about Flux and GitOps best practices,
get to know the team and join our community.

### Flux Bug Scrub

Our Flux Bug Scrubs still are happening on a weekly basis and remain one
of the best ways to get involved in Flux. They are a friendly and
welcoming way to learn more about contributing and how Flux is organised
as a project.

The next dates are going to be:

- [2023-03-02 18:00 UTC, 19:00 CEST](/#calendar)
- [2023-03-08 12:00 UTC, 14:00 CEST](/#calendar)
- [2023-03-16 18:00 UTC, 19:00 CEST](/#calendar)
- [2023-03-22 12:00 UTC, 14:00 CEST](/#calendar)

We are flexible with subjects and often go with the interests of the
group or of the presenter. If you want to come and join us in either
capacity, just show up or if you have questions, reach out to Kingdon on
Slack.

We really enjoyed this [demo of the k3d git
server](https://www.youtube.com/watch?v=hNt3v0kk6ec)
recently. It's a local Git server that runs outside of Kubernetes, to
support offline dev in a realistic but also simple way that does not
depend on GitHub or other hosted services.

## In other news

### Gitlab

{{< tweet user="stefanprodan" id="1618655919449206785" >}}

- <https://about.gitlab.com/blog/2023/02/08/why-did-we-choose-to-integrate-fluxcd-with-gitlab/>

### Your Community Team

### People writing/talking about Flux

We love it when you all write about Flux and share your experience,
write how-tos on integrating Flux with other pieces of software or other
things. Give us a shout-out and we will link it from this section! ✍

- <https://testkube.io/blog/flux-testkube-gitops-testing-is-here>

### News from the Website and our Docs

#### Flux Adopters shout-out

We are very pleased to announce that the following adopters of Flux have
come forward and added themselves to our website: [Wildlife
Studios](https://wildlifestudios.com/).

If you have not already done so, [use the instructions
here](/adopters/) or give us a ping and we will help to add you. Not only
is it great for us to get to know and welcome you to our community. It
also gives the team a big boost in morale to know where in the world
Flux is used everywhere.

#### More docs and website news

We are constantly improving our documentation and website - here are a
couple of small things we landed recently:

- Michel Bridgen wrote a blog post about [how to combine Pulumi with
  Flux](/blog/2023/02/flux-pulumi-superpowers/), which gives each of
  the tools super powers.
- We updated the docs to reflect current Flux version and fixed typos
  and readability pieces in many many places.
- We updated our [Security Docs](/flux/security).

Thanks a lot to these folks who contributed to docs and website: Ben
Bodenmiller, Stefan Prodan, Michael Bridgen, Kingdon Barret, Mac Chaffee,
Ronan.

## Flux Project Facts

We are very proud of what we have put together. We want to reiterate
some Flux facts - they are sort of our mission statement with Flux.

1. 🤝 Flux provides GitOps for both apps or
  infrastructure. Flux and [Flagger](https://github.com/fluxcd/flagger)
  deploy apps with canaries, feature flags, and A/B rollouts. Flux
  can also manage any Kubernetes resource. Infrastructure and workload
  dependency management is built-in.
1. 🤖 Just push to Git and Flux does the rest. Flux
  enables application deployment (CD) and (with the help of
  [Flagger](https://github.com/fluxcd/flagger))
  progressive delivery (PD) through automatic reconciliation. Flux
  can even push back to Git for you with automated container image
  updates to Git (image scanning and patching).
1. 🔩 Flux works with your existing tools: Flux works with your Git
   providers (GitHub, GitLab, Bitbucket, can even use s3-compatible
   buckets as a source), all major container registries, fully
   integrates [with OCI](/flux/cheatsheets/oci-artifacts) and all CI
   workflow providers.
1. 🔒 Flux is designed with security in mind: Pull vs. Push,
  least amount of privileges, adherence to Kubernetes security
  policies and tight integration with security tools and
  best-practices. Read more about our security considerations.
1. ☸️ Flux works with any Kubernetes and all common Kubernetes
  tooling: Kustomize, Helm, RBAC, and policy-driven
  validation (OPA, Kyverno, admission controllers) so it simply
  falls into place.
1. 🤹 Flux does Multi-Tenancy (and "Multi-everything"):
  Flux uses true Kubernetes RBAC via impersonation and supports
  multiple Git repositories. Multi-cluster infrastructure and apps
  work out of the box with Cluster API: Flux can use one Kubernetes
  cluster to manage apps in either the same or other clusters, spin
  up additional clusters themselves, and manage clusters including
  lifecycle and fleets.
1. ✨ Dashboards love Flux: No matter if you use one of
   [the Flux UIs](/ecosystem/#flux-uis--guis) or a hosted cloud
   offering from your cloud vendor, Flux has a thriving ecosystem
   of integrations and products built on top of it and all have
   great dashboards for you.
1. 📞 Flux alerts and notifies: Flux provides health
  assessments, alerting to external systems and external events
  handling. Just "git push", and get notified on Slack and [other
  chat systems](/flux/components/notification/provider/).
1. 👍 Users trust Flux: Flux is a CNCF Graduated project
  and was categorised as "Adopt" on the [CNCF CI/CD Tech
  Radar](https://radar.cncf.io/2020-06-continuous-delivery)
  (alongside Helm).
1. 💖 Flux has a lovely community that is very easy to work
  with! We welcome contributors of any kind. The
  components of Flux are on Kubernetes core controller-runtime, so
  anyone can contribute and its functionality can be extended very
  easily.

## Over and out

If you like what you read and would like to get involved, here are a few
good ways to do that:

- Join our [upcoming dev meetings](/community/#meetings) on
  2023-03-09 or 2023-03-15.
- Talk to us in the #flux channel on [CNCF Slack](https://slack.cncf.io/)
- Join the [planning discussions](https://github.com/fluxcd/flux2/discussions)
- And if you are completely new to Flux, take a look at our [Get
  Started guide](/docs/get-started/) and give us feedback
- Social media: Follow [Flux on Twitter](https://twitter.com/fluxcd),
  join the discussion in the [Flux LinkedIn
  group](https://www.linkedin.com/groups/8985374/).

We are looking forward to working with you.
