C3-PRO Modules
==============

This repository contains metadata to software modules that are capable of tying into the [C3-PRO](http://c3-pro.chip.org) toolchain.

Module Description
------------------

Each module is described in a simple _JSON_ file, named in recursive URI style, in the `modules` directory.
For example, our iOS framework is described like this:

```
{
  "name": "C3-PRO iOS Framework",
  "short": "This iOS framework allows you to use FHIR resources…",
  "description": "Combining 🔥 FHIR and ResearchKit, the iOS framework…",
  "web": "https://github.com/chb/c3-pro-ios-framework",
  "git": "https://github.com/chb/c3-pro-ios-framework.git",
  "docs": "http://chb.github.io/c3-pro-ios-framework/",
  "author": {
    "name": "CHIP, Boston Children’s Hospital",
    "web": "http://chip.org",
    "contact": "somebody@childrens.harvard.edu"
  },
  "type": [
    "mobile"
  ],
  "technologies": [
    "iOS",
    "ResearchKit",
    "Swift"
  ],
  "interfaces": {
    "input": [
      "FHIR Resources",
      "Particpant Input",
      "Sensor Data",
      "Geodata"
    ],
    "output": [
      "FHIR Resources",
      "Encrypted FHIR Resources"
    ]
  },
  "license": "APACHE II"
}
```

Most keys should be self-explanatory, some explanations:

- `short` must be a short description of what your project does, limited to 100 characters. If omitted, the first 99 chars of the _description_ may be used.
- `description` describes your module in a couple of sentences
- `author`
  + `name` is the name of you or your organization
  + `web` a link to your website (optional)
  + `contact` where you or somebody else can be reached (optional)
- `type` can be any combination of:
  + `mobile` means the module runs on the mobile phone
  + `www` means the module is accessible from the www
  + `backend` means the module is designed to run behind a firewall
  + `storage` means the module is capable of storing (and possibly serving) data
- `interfaces`
  + `input` describes what the module can work with, if any, in 1-3 words each
  + `output` defines what the outputs of the module are, if any, in 1-3 words each
- `technologies` describe the main technologies and platforms used. Use what you think helps deciding whether your module is a fit; take a look at existing modules to re-use keywords.

Contributing
------------

Have a module that can tie into C3-PRO?
Fork this repo, add your module's JSON file to `modules` and issue a pull request!
