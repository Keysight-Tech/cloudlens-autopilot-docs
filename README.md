# CloudLens AutoPilot for AWS

**Customer-facing documentation site for the Keysight CloudLens AutoPilot AWS automation platform.**

🌐 **Live site:** https://keysight-tech.github.io/cloudlens-autopilot-docs/

This repository hosts the public landing site, runbooks, CloudFormation templates, and supporting docs for the CloudLens AutoPilot project. The source-code IaC (Terraform modules, Lambda functions, SSM Documents) lives in the private `Keysight-Tech/cloudlens-autopilot` repo.

## What is CloudLens AutoPilot?

A turn-key automation platform that deploys the full Keysight CloudLens visibility stack on AWS in under 10 minutes:

- ✅ **KVO** (Keysight Vision One) — master orchestrator
- ✅ **CLMS** (CloudLens Manager) — sensor management
- ✅ **vPB** (Virtual Packet Broker) — traffic processing
- ✅ **Auto-Mirror Lambda** — instant EventBridge-driven VPC Traffic Mirroring
- ✅ **SSM-based sensor rollout** — push CloudLens sensors to every tagged EC2 instance with no SSH, no WinRM

## Quick start

| Path | When to use |
|---|---|
| [▶ Deploy via AWS Console](https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/review?templateURL=https://raw.githubusercontent.com/Keysight-Tech/cloudlens-autopilot-docs/main/cloudlens-autopilot.yaml&stackName=cloudlens-autopilot) | Easiest. Click, fill parameters, watch it deploy. |
| `terraform apply -var-file=demo.tfvars` | SE / DevOps workflow with state management. |
| AWS Marketplace subscriptions first | One-time per AWS account, then either path above works. |

## What's in this repo

| File | Purpose |
|---|---|
| [`index.html`](index.html) | Single-page documentation site (served at `keysight-tech.github.io/cloudlens-autopilot-docs/`) |
| [`cloudlens-autopilot.yaml`](cloudlens-autopilot.yaml) | Greenfield CloudFormation template (creates new VPC) |
| [`cloudlens-existing-vpc.yaml`](cloudlens-existing-vpc.yaml) | Brownfield CloudFormation template (deploys into customer VPC) |
| [`CloudLens-AutoPilot-Deployment-Runbook.docx`](CloudLens-AutoPilot-Deployment-Runbook.docx) | Full 10-section customer runbook (1,462 lines) |
| [`CloudLens-AutoPilot-Existing-VPC-Runbook.docx`](CloudLens-AutoPilot-Existing-VPC-Runbook.docx) | Brownfield variant runbook |
| [`CloudLens-AutoPilot-Executive-Summary.docx`](CloudLens-AutoPilot-Executive-Summary.docx) | 3-page exec summary (AAA case study, Gigamon comparison) |
| [`ARCHITECTURE.md`](ARCHITECTURE.md) | Architecture overview + data flow |
| [`DEPLOYMENT_GUIDE.md`](DEPLOYMENT_GUIDE.md) | Step-by-step deployment guide (CFT + Terraform paths) |
| [`SCALING.md`](SCALING.md) | Sensor fleet scaling guidance (1 → 15,000+ VMs) |
| [`TROUBLESHOOTING.md`](TROUBLESHOOTING.md) | Common errors and fixes |
| [`CUSTOMER_EMAIL.md`](CUSTOMER_EMAIL.md) | Template email SEs can send customers |

## AWS Marketplace prerequisites

Subscribe **once per AWS account** to the 3 Keysight products:

1. [Keysight Vision One](https://aws.amazon.com/marketplace/search/results?searchTerms=Keysight+Vision+One) — `c5.2xlarge` only
2. [Keysight CloudLens Manager](https://aws.amazon.com/marketplace/search/results?searchTerms=Keysight+CloudLens+Manager) — `t3.xlarge`
3. [Keysight CloudLens Virtual Packet Broker](https://aws.amazon.com/marketplace/search/results?searchTerms=Keysight+CloudLens+Virtual+Packet+Broker) — `t3.xlarge` only

## Customer case studies in production

- **AAA Financial Services** — 847 VMware VMs, Ansible Tower, 45-minute end-to-end deploy
- **Nokia** — 4G LTE private network, CMU containerized, E40 packet broker, VIAVI TSA
- **Airtel** — OpenShift 4.x with OVN-Kubernetes; projected 1,700-site E1S/E50 rollout

## License

MIT — see [LICENSE](LICENSE).

## Contact

- 🐛 [Issues](https://github.com/Keysight-Tech/cloudlens-autopilot-docs/issues)
- 🌐 [Keysight Technologies](https://www.keysight.com)
