# Dracut & Initramfs Guide

## Table of Contents
- [Introduction](#introduction)
- [Initramfs](#initramfs)
- [Dracut](#dracut)
- [Usage](#usage)


## Introduction
This guide provides an overview of `dracut` and `initramfs`, essential components in the Linux boot process.

## Initramfs

**initramfs** stands for "initial RAM filesystem." It is a temporary root filesystem loaded into memory during the Linux boot process before the actual root filesystem is mounted.

### Purpose:
- Prepare the system to mount the real root filesystem.
- Load necessary disk drivers, set up device nodes, or perform other early-stage system initialization tasks.
- Essential when the root filesystem is on an LVM, RAID array, or requires specific drivers/modules.

## Dracut

**dracut** is a universal initramfs generation tool used across various Linux distributions. It creates the `initramfs` image.

### Key Features:
- Modular: Only includes the modules and tools necessary for the boot process.
- Universal: Can be used across various Linux distributions.
- Customizable: Can be tailored to include or exclude specific modules or tools.

## Usage

To generate a new `initramfs` image using `dracut`:

```bash
dracut --force
