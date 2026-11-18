# Letterboxed Video Before Upscaling: Crop the Bars First, and Prove It

A 1920×1080 frame holding a 1440×1080 picture has 25% of its pixels doing nothing. Measured: upscaling the full frame first costs 1.37× the compute and contaminates 3.5 source pixels at the active edge — but a whole-frame PSNR moves only 0.01 dB, so the metric cannot see it. Also measured: cropdetect's threshold is a truncated mean, not a maximum, so a bar is defeated by lighting 105 of its 1080 rows, not by one bright pixel.

**Read it with the tables and the reproduction snippets:** <https://celticgemini001.github.io/upgolab-letterbox-before-upscale/>

## About this repo

This repository exists to serve one measured article. Every number in it came from
ffmpeg and numpy run on real files on this machine — the commands are in the page so
you can re-run them and get the same rows. Where the measurement contradicted the
hypothesis, the page says so.

## The tool behind the notes

<https://upgolab.com> — browser-based AI upscaler for photos and short video.

## Index

All the guides are cross-linked from the hub:
<https://celticgemini001.github.io/upgolab-tools/>
