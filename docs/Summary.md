# Copyright (c) 2016-2021 Martin Donath <martin.donath@squidfunk.com>

# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to
# deal in the Software without restriction, including without limitation the
# rights to use, copy, modify, merge, publish, distribute, sublicense, and/or
# sell copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:

# The above copyright notice and this permission notice shall be included in
# all copies or substantial portions of the Software.

# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
# FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
# IN THE SOFTWARE.
# Page tree
nav:
#  - Bassics: basics/Purpose.md
  - About: about/who-am-i.md
  - Looking across clouds: basics/cloud-provider-service-summary.md
  - Cross Cloud Notes:
      - Purpose: common-notes/purpose.md
      - Security Control Model: common-security/threat-models.md
      - Understanding Kafka:  common-notes/kafka.md
      - Understanding K8S request & limits: common-notes/understanding-k8s-requests-limits.md
      - Crossplane IAC: common-notes/crossplane-IaC.md
      - Logging in K8S: common-notes/kubernetes-logging.md
      - Operators: common-notes/operators.md
      - K8S how it works: common-notes/how-k8s-works.md
      - Understanding VPNs: common-notes/understanding-VPNs.md
      - Understanding Akamai: common-notes/understanding-dns-akamai.md
      - A perspective on Analytics: common-notes/view-of-analytics.md
      - Understanding ELK: common-notes/understanding-elk.md
      - Understanding Docker and K8S: common-notes/understanding-docker-k8s.md
      - MicroServices: microservice-blog/about.md
      - Digital Exhaust & Compliance: common-notes/digital-exhaust-compliance.md
      - What is DAPR?: common-notes/dapr.md
      - REST vs GRPC: common-notes/rest-grpc.md
  - Microservices:
      - About:  microservice-blog/about.md
      - Microservices "On Hold": microservice-blog/onhold.md
      - Microservice SKUs: microservice-blog/sku.md
      - Event and Stateflows:  microservice-blog/events-stateflows.md
      - Service Brokers: microservice-blog/service-brokers.md
      - Microservice Vending Machine:  microservice-blog/vending-machine.md
      - Con-Ed?: microservice-blog/con-ed.md
      - Utility Infrastructures?: microservice-blog/utility-infrastructure.md
      - The "butler" microservice: microservice-blog/alfred.md
      - Continuous Delivery: microservice-blog/continuous.md
      - A Point of view:  microservice-blog/what-how.md
      - Shiny Objects:  microservice-blog/shiney-object.md
      - Its all about events:  microservice-blog/events.md
      - Distribution of Microservices: microservice-blog/distribution.md
      - Ramping up - Scaling Microservices: microservice-blog/rampingup.md
      - All about the Data: microservice-blog/data.md
      - Legos?:  microservice-blog/legos.md
      - Containers: microservice-blog/containers.md
      - Origins: microservice-blog/origins.md
      - Seven Things: microservice-blog/seventhings.md
      - Fundamentals: microservice-blog/fundamentals.md
      - Forte':  microservice-blog/forte.md
  - IT Architecture:
      - Purpose: architecture/purpose.md
      - 4 Key Things: architecture/four-things.md
      - Getting Your Message Across: architecture/communicating-message.md
  - AWS:
      - Purpose: cloud-aws-cloud/Purpose.md
      - Organizations and Accounts: cloud-aws-cloud/understanding-regions-accounts.md
      - Regional Services View: cloud-aws-cloud/understanding-regions-services.md
      - Operations Management: cloud-aws-cloud/ops-mgmt.md
      - Security:
          - IAM: cloud-aws-cloud/security-iam.md
          - Assume Role: cloud-aws-cloud/assume-role.md
          - Controls and Auditing: cloud-aws-cloud/security-services.md
          - Key Management: cloud-aws-cloud/key-management-services.md
#          - Params and Secrets:  cloud-aws-cloud/params-secrets.md
      - Compute and Storage:
          - EC2 & AutoScaling: cloud-aws-cloud/ec2.md
          - Spot Instances: cloud-aws-cloud/ec2-spot.md
          - Placement Groups: cloud-aws-cloud/ec2-placement.md
          - EBS and EFS: cloud-aws-cloud/storage-ebs-efs.md
          - Storage Gateway: cloud-aws-cloud/storage-gateway.md
          - S3:  cloud-aws-cloud/s3.md
          - Containers & K8S: cloud-aws-cloud/containers.md
      - Networking:
          - VPC Overview: cloud-aws-cloud/network-services.md
          - VPC Connectivity: cloud-aws-cloud/connectivity-services.md
          - DNS, ENI, etc...: cloud-aws-cloud/connectivity-etc.md
          - CloudFront & Global Accelerator: cloud-aws-cloud/network-cloudfront.md
      - Data and Analytics:
          - Integration via Qs & Streams:  cloud-aws-cloud/integation.md
          - Databases: cloud-aws-cloud/databases.md
          - Caching: cloud-aws-cloud/elasticache.md
          - Data Replication, Backup, Sync: cloud-aws-cloud/data-replication.md
          - Data Integration: cloud-aws-cloud/data-integration.md
          - Data-Lakes: cloud-aws-cloud/data-lakes.md
      - Other:
          - Events: cloud-aws-cloud/event-bridge.md
          - Serverless: cloud-aws-cloud/serverless.md
          - CloudWatch: cloud-aws-cloud/cloudwatch.md
  - Google Cloud:
      - Purpose: cloud-google-cloud/Purpose.md
      - Basics:
          - Fundamentals of GCP: cloud-google-cloud/fundamentals.md
          - Google Architecture Framework: cloud-google-cloud/arch-framework.md
      - Org, Projects, and IAM:
          - Basics: cloud-google-cloud/understanding-regions-accounts.md
          - IAM: cloud-google-cloud/iam.md
          - Service and Host Projects: cloud-google-cloud/project-details.md
      - Data & Analytics:
          - Big Query: cloud-google-cloud/gcp-big-query.md
          - Data Lakes: cloud-google-cloud/gcp-big-data.md
      - Containers and K8S:
          - GKE: cloud-google-cloud/kubernetes-engine.md
      - Networking:
          - Overall Subject Area: cloud-google-cloud/network-services.md
          - Connectivity:  cloud-google-cloud/connectivity.md
      - Compute Engine:  cloud-google-cloud/compute-engine.md
  - MS Azure:
      - Purpose: cloud-microsoft-cloud/Purpose.md
      - Fundamentals: cloud-microsoft-cloud/fundamentals.md
      - Resource Overview: cloud-microsoft-cloud/resource-overview.md
  - IBM Cloud:
      - Purpose: cloud-ibm-cloud/Purpose.md
      - Regions and Accounts: cloud-ibm-cloud/understanding-regions-accounts.md
      - Networking: cloud-ibm-cloud/network-services.md
      - Security: cloud-ibm-cloud/security-services.md
      - Key Management: cloud-ibm-cloud/key-management-services.md

  - Patterns:
      - Event Driven Solutions: patterns/event-driven-1.md
      - Microservice Integration: patterns/microservice-integration.md
# Project information
site_name: Cloud Notebook
site_url: https://pkkyndryl.github.io/cloud-notebook/
site_author: Gary Zeien
site_description: >-
  A notebook containing information on how Cloud Providers work.

# Repository
repo_name: Gzeien/cloud-notebook
repo_url: https://pkkyndryl.github.io/cloud-notebook
edit_uri: ""

# Copyright
copyright: Copyright &copy; 2021 - 2024 Gary Zeien

# Configuration
theme:
  name: null
  custom_dir: !ENV [THEME_DIR, "material"]

  # Static files
  static_templates:
    - 404.html

  # Don't include MkDocs' JavaScript
  include_search_page: false
  search_index_only: true

  # Default values, taken from mkdocs_theme.yml
  language: en
  features:
    - content.code.annotate
    - content.tabs.link
    # - header.autohide
    # - navigation.expand
    # - navigation.indexes
    # - navigation.instant
    - navigation.sections
    - navigation.tabs
    - navigation.tabs.sticky
    - navigation.top
    - navigation.tracking
    - search.highlight
    - search.share
    - search.suggest
    - toc.integrate
  palette:
    - scheme: default
      primary: indigo
      accent: indigo
      toggle:
        icon: material/toggle-switch
        name: Switch to dark mode
    - scheme: slate
      primary: red
      accent: red
      toggle:
        icon: material/toggle-switch-off-outline
        name: Switch to light mode
  font:
    text: Roboto
    code: Roboto Mono
  favicon: assets/logo.png
  logo: assets/logo.png
  icon:
    logo: logo

extra_css:
  - 'extra.css'
  - 'extra-pagesize.css'

# Plugins
plugins:
  - search
  - git-revision-date-localized
#  - redirects:
#      redirect_maps:
#        changelog/insiders.md: insiders/changelog.md
#        reference/meta-tags.md: reference/index.md
#        reference/variables.md: https://mkdocs-macros-plugin.readthedocs.io/
#        sponsorship.md: insiders/index.md
#        upgrading.md: upgrade.md
  - minify:
      minify_html: true

# Customization


# Extensions
markdown_extensions:
  - admonition
  - abbr
  - attr_list
  - def_list
  - footnotes
  - meta
  - md_in_html
  - toc:
      permalink: true
  - pymdownx.arithmatex:
      generic: true
  - pymdownx.betterem:
      smart_enable: all
  - pymdownx.caret
  - pymdownx.details
  - pymdownx.emoji:
      emoji_index: !!python/name:materialx.emoji.twemoji
      emoji_generator: !!python/name:materialx.emoji.to_svg
  - pymdownx.highlight:
      anchor_linenums: true
  - pymdownx.inlinehilite
  - pymdownx.keys
  - pymdownx.magiclink:
      repo_url_shorthand: true
      user: squidfunk
      repo: mkdocs-material
  - pymdownx.mark
  - pymdownx.smartsymbols
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_code_format
  - pymdownx.tabbed:
      alternate_style: true
  - pymdownx.tasklist:
      custom_checkbox: true
  - pymdownx.tilde
