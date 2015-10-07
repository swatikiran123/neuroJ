# neuroJ

#Introduction

Project Hanlon is a power control, provisioning, and management application designed to deploy both bare-metal and virtual computer resources. Hanlon provides broker plugins for integration with third party such as Puppet.

Hanlon started its life as Razor so you may encounter links to original created-for-Razor content. The following links, for example, provide background info about the project:

    

- Razor Overview: Nickapedia.com
-  Razor Session from PuppetConf 2012: Youtube

Project Hanlon is versioned with semantic versioning, and we follow the precepts of that document.

#How to contribute

We really want Hanlon to be simple to contribute to, and to ensure that you can get started quickly. A big part of that is being available to help you figure out the right way to solve a problem, and to make sure you get up to speed quickly.

You can always reach out and ask for help by email or through the web on the hanlon-project@googlegroups.com mailing list. (membership is required to post.)

If you want to help improve Hanlon directly we have a fairly detailed CONTRIBUTING guide in the repository that you can use to understand how code gets in to the system, how the project runs, and how to make changes yourself.

We welcome contributions at all levels, including working strictly on our documentation, tests, or code contributions. We also welcome, and value, input about your experiences with Project Hanlon, and provisioning in general, on the mailing list as we discuss how the project might solve these sorts of problems.
#Installation

Follow wiki documentation for Installation Overview
#Project Committers
<
This is the official list of users with "committer" rights to the Hanlon project. For details on what that means, see the CONTRIBUTING guide in the repository

    

- Nicholas Weaver
- Tom McSweeney
- Nan Liu

If you can't figure out who to contact, Tom McSweeney is the best first point of contact for the project. (Find me at Tom McSweeney tjmcs@bendbroadband.com)

This is a hand-maintained list, thanks to the limits of technology. Please let Tom McSweeney know if you run into any errors or omissions in that list.
#Hanlon MicroKernel

Hanlon uses an associated Hanlon-Microkernel instance to discover new nodes. Pre-build images of the current Hanlon-Microkernel (v2.0.1) are officially available at:

https://github.com/csc/Hanlon-Microkernel/releases/tag/v2.0.1

On that page, you will find three Microkernel images (hnl_mk_debug-image.2.0.1.iso, hnl_mk_dev-image.2.0.1.iso and hnl_mk_prod-image.2.0.1.iso). Those correspond to the debug, development and production Microkernels (respectively). The difference between them is as follows:

    

- debug

    In a debug Microkernel, remote access to the Microkernel is allowed for the tc user via SSH. The tc user is also logged into the Microkernel instance automatically when the node boot process is complete. This Microkernel is useful for debugging problems with the process of booting and reporting in to the Hanlon server, but should not be used in production.

    

- development

    In a development Microkernel, remote access to the Microkernel is allowed for the tc user via SSH. Local access (via the console) is also enabled for the tc once the node boot process is complete, but a password is required. This Microkernel type is useful for developers working on Hanlon, where remote access to the Microkernel might be required. While slightly more secure than the debug Microkernel (above), this Microkernel is also one that is not intended for use in a production.

    

- production

    In a production Microkernel, remote access to the Microkernel is disabled completely, as is local access (via the console). This Microkernel is intended for use in a production environment, where access to the resources of the underlying node through the Microkernel could prove to be a security risk. Obviously, disabling local and remote access to the Microkernel makes this type of Microkernel unsuitable for development (on either Hanlon or the Hanlon-Microkernel).

You can find more information on the Microkernel and on the process for building your own Microkernel images at the Hanlon MicroKernel project page:

https://github.com/csc/Hanlon-Microkernel
#License

Project Hanlon is distributed under the Apache 2.0 license. See the LICENSE file for full details.
#Reference

The following links contain useful information on the Hanlon (and Hanlon-Microkernel) projects as well as information on the new CSC Open Source Program:

    

- Tom McSweeney's blog entry on the availability of this project: Announcing Hanlon and the Hanlon-Microkernel
-  Dan Hushon's blog entry on the new CSC Open Source Program: Finding Value in Open Source
- A blog posting by Tom McSweeney describing the changes that went into the Hanlon 2.0 Release in October, 2014
- Tom's blog entry from March, 2015 announcing support for Windows provisioning in Hanlon (Hanlon does Windows!) along with the associated screencast by Tom demonstrating this Windows support

Finally, these links provide an introduction to the original Razor project (and, given Hanlon's roots in the original Razor project, they may be of interest to those new to the Razor/Hanlon community):

    

- The original Razor Overview posting: Nickapedia.com
- A video of Nick Weaver's Razor Session from PuppetConf 2012: Youtube
- The original posting by Nan Liu describing the first Puppet Labs Razor Module: Puppetlabs.com

Even though the Puppet Labs module described in the last link is no longer maintained, and even though it doesn't support Hanlon, we included it here because we felt that the information in that blog posting may provide useful to those who would like to develop a corresponding Hanlon module.
