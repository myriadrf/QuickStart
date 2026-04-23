Introduction
############

.. toctree::
   :maxdepth: 2
   :hidden:

   Introduction <self>

The SDR Quick Start Guide provides an overview of the steps required to get up and running with LimeSDR software-defined radio platforms, along with the software options which are available for use with them. 

.. note::
   This guide is a work-in-progress, initially providing basic guidance and links to relevant software, and will be updated over time. 

Supported Operating Systems
***************************

Linux is the primary supported operating system for LimeSDR hardware. Windows is also supported with USB-based devices, but is presently unsupported with PCIe SDRs due to a current lack of driver support.

.. note::
   Some Windows applications distribute the Lime Suite DLL as part of their installation, meaning that it may not be neccessary to install the Lime Suite software package separately in order to use such applications. 

There is some support for using LimeSDR hardware with macOS, FreeBSD, and possibly other UNIX-like operating systems, but this is not currently a focus of development, and any support will be via community efforts. Contributions to improve support for such platforms and to add support for new operating systems are welcome, but may not be actively developed or supported by Lime Microsystems.

Lime Suite vs. Lime Suite NG
****************************

LimeSDR hardware is supported by the Lime Suite software package, which provides drivers and tools for configuring and using LimeSDR devices. The Lime Suite software is available for Linux and Windows operating systems, and it can be used to control and operate a wide range of LimeSDR devices.

There are two versions of the Lime Suite software available: the original Lime Suite, and the newer Lime Suite NG (Next Generation).

The original Lime Suite — sometimes referred to as *legacy* or *classic* Lime Suite — is a mature software package that provides support for a wide range of LimeSDR devices, but it is no longer actively developed and is now in maintenance mode. 

Lime Suite NG is a more recent software package that is actively developed and provides various new features, plus support for the latest LimeSDR hardware, but it may not have all the features of the original Lime Suite.

.. list-table:: SDR Device Support Matrix
   :header-rows: 1

   * - Device
     - Lime Suite
     - Lime Suite NG
     - Windows Support
     - Notes
   * - LimeSDR Micro
     - No
     - Yes
     - No
     -
   * - LimeSDR X3
     - No
     - Yes
     - No
     -
   * - LimeNET Micro 2.0 
     - No
     - Yes
     - No
     - Based on LimeSDR XTRX
   * - LimeSDR XTRX
     - No
     - Yes
     - No
     -
   * - LimeSDR Mini 2.0
     - Yes
     - Yes
     - Yes
     -
   * - LimeNET Micro
     - Yes
     - No
     - No
     - 
   * - LimeSDR Mini
     - Yes
     - Yes
     - Yes
     - 
   * - LimeSDR USB
     - Yes
     - Yes
     - Yes
     -
   * - LimeSDR PCIe
     - Yes
     - No
     - Yes
     - Windows support via Xillybus driver

Which should I use?
===================

End Users
---------

As an end user this will come down to a combination of whether you are using a device which is supported by one or the other, and whether the applications you wish to use are supported by Lime Suite or Lime Suite NG.

If you are using a newer device which is only supported by Lime Suite NG, then you will need to use that. If you are using an older device which is supported by both, then you may have to use the original Lime Suite if the applications you wish to use do not yet have support for Lime Suite NG.

In some cases you may have both options available to you. For example, Lime Suite and Lime Suite NG both provide support for LimeSDR Mini 2.0, and both have plugins for SoapySDR and GNU Radio. Hence if you intended to use a LimeSDR Mini 2.0 with an application based on GNU Radio or with SoapySDR support, both driver stack options would be available to you. In such cases it would be recommended to use Lime Suite NG, as it is the more modern and actively developed software package, and will likely have support for new features and devices.

Developers
----------

Developers of new applications should always use Lime Suite NG where possible. This will ensure that their applications are compatible with the latest devices and able to benefit from the latest driver features and improvements.

.. note::
   Lime Suite NG includes a compatibility layer for applications which were developed for use with the original Lime Suite, but these may still require some changes in order to be used with NG and the legacy LMS API wrapper will not be supported indefinitely. 
   
   As such it is recommended to use the native Lime Suite NG API (SDRDevice) for new applications wherever possible.

Links
*****

