---
layout: post
title: IITPipe Driver - Building a Custom Kernel Module for Delayed Piping
---

Piping is a powerful feature in Unix-like operating systems that allows programs to communicate with each other, passing data from the output of one program to the input of another. However, standard piping is instantaneous, with no delay between the two programs. This can lead to issues if the programs require a delay between them, such as for synchronization or testing purposes. To address this issue, we have implemented a custom kernel module, IITPipe Driver, which provides delayed piping capabilities.

The IITPipe Driver module works by adding a configurable delay between the output of one program and the input of the next. This delay is implemented using a buffer, which stores the data from the first program until the delay period has passed, at which point it is passed on to the second program. The module is built using the Linux kernel's module interface, allowing it to be loaded and unloaded dynamically as needed.

To measure the performance of the IITPipe Driver module, we conducted a series of tests using different delay and buffer sizes. We measured the time it took for data to pass through the pipe and compared it to the same data passed through a standard pipe with no delay. Our results showed that the IITPipe Driver module added a measurable delay, with longer delays resulting in longer processing times. However, even with significant delays, the performance of the IITPipe Driver module was still comparable to that of a standard pipe.

The IITPipe Driver module has several potential use cases, including in synchronization and testing scenarios. For example, it could be used to simulate network latency for testing networked applications. It could also be used to coordinate the timing of multiple programs, ensuring that they execute in a specific order.