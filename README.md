# PulseChain Projects Repository
Open Source repository of PulseChain and HEX-related products, projects, site and tokens in machine processable form (YAML).
This documentation uses for simplicity term _project_ do denote all types of entities described in this repository.

# Data Structure
Each project (product, site, or token) is described by a single file in the `data/` subdirectory.
Each file is in [YAML](https://yaml.org/) format, with `.yaml` extension, starting with `---` signature.

Allowed root keys:
  - `name` - (mandatory) a human readable name of the project.
  - `status` - (mandatory) enumeration describing stage of implementation and deployment, allowed values are:
    - `promise` - the project exists mostly on paper or community is building.
    - `active` - project is in active development with publicly available artifacts (application previews, progress reports, community discussion and polls, etc.).
    - `completed` - project was fully completed and waits for its final deployment.
    - `usable` - project turned into product and can be used of bought on market.
    - `dormant` - project community is quite silent, there are no real updates from the project team.
    - `abandoned` - project community is completely silent, project team does not respond in a timely manner.
    - `terminated` - project was terminated, without usable artifiacts.
    - `rugged` - there are clear signs that project was rug pulled (social media channel closed, liquidity suddenly removed, etc.).
    - `scam` - there are clear signs that project was a scam.
  - `description` - long description of the project.
  - `www` - fully qualified URL to main page of the project.
  - `categories` - describes detailed metadata about projects' "sacrifice" TBD.
  - `socials` - describes social media accounts related to this project, each social media is associated with a key.
    Please note, that values of this dictionary are not URLs but only account identifiers.  
    Allowed keys are:
    - `twitter` - account for Twitter.
    - `tg` - account for Telegram.
    - `fb` - account for Facebook.
    - `yt` - account for YouTube.
    - `ig` - account for Instagram.
    - `email` - primary contact email address.
    - `github` - account for GitHub.
    - `reddit` - account for Reddit.
    - `medium` - account for Medium.
    - `discord` - account for Discord.
  - `links` - array of links related to the project.
    Each link has structure `<link-type>: <link-url>`, where type can be potentially any identifier.
    Same type of link can be used multiple types.  
    Recommended link types are:
    - `app` - link to mobile app.
    - `dapp` - link to dApp web site.
    - `docs` - link to web site project documentation.
    - `audit` - link to projects audit report.
    - `kyc` - link to KYC certificate for project or project members.
  - `sacrifice` - describes detailed metadata about projects' "sacrifice" TBD.
  - `token` - describes detailed metadata about the token related to this project TBD.

