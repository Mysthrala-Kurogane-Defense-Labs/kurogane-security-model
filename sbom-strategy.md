# Software component inventory and SBOM review

## Purpose and boundary

An SBOM describes components of an identified artifact. It does not prove that the artifact is secure, that no advisory applies or that an installation runs that version. This repository publishes a review strategy, not an SBOM for the private Hub.

## Minimum review package

Request artifact name/version and hash, repository commit, generation tool/version/date, component names/versions/identifiers, direct and transitive relationships, licenses, and stated completeness limitations. Include runtimes, base images and system packages where relevant; zero Elixir dependencies does not mean zero runtime components.

Use an agreed machine-readable specification such as [SPDX](https://spdx.dev/use/specifications/) or [CycloneDX](https://cyclonedx.org/specification/overview/). Record the selected specification version and validate the document against it.

## Verification

Compare the inventory with lockfiles, build inputs and the delivered image/artifact. Review advisories at a stated date and retain disposition evidence for each affected component. A digest makes an image identifiable; it does not eliminate the need for update and advisory review.

## Output

An inventory tied to an immutable artifact plus a separate vulnerability-review record. Mark omitted components and unsupported claims. No signed provenance, published private SBOM or automatic update service is claimed here.
