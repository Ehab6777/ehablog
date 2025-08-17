---
title: "Why I think Java auto-cinfiguration better than Rust"
date: 2025-08-16
draft: false
description: "This is a short description of my post."
tags: ["programming", "tutorial"]
categories: ["Tech"]
---
The other day I had a discussion with someone about how to implement FFT-based convolution/polynomial multiplication - they were having a hard time squeezing their library implementation into the time limit on this problem, and it soon turned into a discussion on how to optimize it as much as possible. It turned out that the bit-reversing part of their iterative implementation was taking a pretty large amount of time, so I suggested not using bit-reversal at all, as is done in a few libraries. Since not a lot of people turned out to be familiar with it, I decided to write a post on some ways of implementing FFT and deriving these ways from one another.

I won’t be going into implementing FFT using SIMD since the constant war (pun intended) of constant optimization over at this problem will probably teach you much more than what I can fit in a tutorial, and it deserves a post on its own anyway. Rather, this blog post will look at how you can think about FFT in ways that you might have not thought about before. Whenever it makes sense, I would link to some nice tutorials on FFT that could be helpful in understanding the ideas in greater detail.
