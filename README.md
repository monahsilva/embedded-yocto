# Meta-Layer Challenge

## Comprehensive Documentation

Welcome to our meta-layer changeled! This README file provides detailed
 instructions on setting up the build environment, including our layer,
 and compiling a new image using Yocto Project.
 Please follow the steps outlined below to ensure a smooth build process.

### Step 1: Setting up the Build Environment

1. **Clone the Poky Repository**: Ensure you have Git installed on your
system, then clone the Poky repository.
   git clone -b kirkstone-harbor https://github.com/Harbor-Systems/poky.git
2. **Navigate to the Poky Directory** : cd poky
3. **Clone the Meta-gstreamer1.0 Repository**: Clone the repository meta-gstrea>
   git clone https://github.com/OSSystems/meta-gstreamer1.0.git
4. **Change bblayers.conf File**: nano conf/bblayers.conf
Add the following lines to the file:
BBLAYERS ?= " \
/path/to/poky/meta \
  /path/to/poky/meta-poky \
  /path/to/poky/meta-yocto-bsp \
  /path/to/meta-custom \
 /path/to/meta-gstreamer1.0 \
"
5. **Create the Image**: bitbake core-image-minimal
