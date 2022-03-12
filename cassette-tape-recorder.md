---
layout: page
title: Cassette Tape Recorders
date: 2022-02-28 19:45:00
permalink: /cassette-tape-recorders/
tagline: "Helpful Information & Links for Cassette Tape Recorders"
---

# Tascam Portastudio 414

Some notes for working on and with the Tascam 414 Portastudio 4 Track Recorder deck.

## Generic 5 Second Cassette Loop

This is a generic clear tape loop. The tape has a particular constant warble, to the point a clear sine tone cannot be read out enough to get an exact key difference.

| Tape Speed In | Tape Speed Out | BPM In | BPM Out | Key In | Key Out | Duration |
|---------------|----------------|--------|---------|--------|---------|----------|
| Normal 🕛     | Fast 🕔        | 120    |  163.30 | C3     | ~F3     | 0:03:532 |
| Normal 🕛     | Normal 🕛      | 120    |  118.02 | C3     | ~C3     | 0:04:709 |
| Normal 🕛     | Slow 🕖        | 120    |   95.41 | C3     | ~G#2    | 0:06:024 |

Below are the iZotope RX views of the loop and the Melodyne view of the loop, to see how unstable it is:

![iZotope RX View]({% asset 'cassette-tape-recorder/izotope-rx-view.png' @path %})

![Melodyne View]({% asset 'cassette-tape-recorder/melodyne-view.png' @path %})

## Sony HF 60 High Bias Type 1

An old tape I used in high school Spanish class, not a tape loop but stable enough to get a key.

Sorted by Tape Speed Out:

| Tape Speed In | Tape Speed Out | BPM In | BPM Out | Key In | Key Out    | Multiplier |
|---------------|----------------|--------|---------|--------|------------|------------|
| Slow 🕛       | Slow 🕛        | 120    |   85.63 | C3     | F#2, +15ct |   70.9416% |
| Normal 🕛     | Slow 🕛        | 120    |   99.52 | C3     | A2, -25ct  |   82.9333% |
| Fast 🕔       | Slow 🕛        | 120    |  120.16 | C3     | C3, -2ct   |      ~100% |
| Slow 🕛       | Normal 🕖      | 120    |  103.13 | C3     | A2, +37ct  |   85.9416% |
| Normal 🕛     | Normal 🕛      | 120    |  119.92 | C3     | C3, -2ct   |      ~100% |
| Fast 🕔       | Normal 🕖      | 120    |  144.68 | C3     | D#3, +24ct |  120.5666% |
| Slow 🕛       | Fast 🕔        | 120    |  120.03 | C3     | C3, +1ct   |      ~100% |
| Normal 🕛     | Fast 🕔        | 120    |  146.08 | C3     | D#3, -39ct |  121.7333% |
| Fast 🕔       | Fast 🕔        | 120    |  168.22 | C3     | F#3, +13ct |  140.1833% |

Sorted by Tape Speed In:

| Tape Speed In | Tape Speed Out | BPM In | BPM Out | Key In | Key Out    | Multiplier |
|---------------|----------------|--------|---------|--------|------------|------------|
| Slow 🕛       | Slow 🕛        | 120    |   85.63 | C3     | F#2, +15ct |   70.9416% |
| Slow 🕛       | Normal 🕖      | 120    |  103.13 | C3     | A2, +37ct  |   85.9416% |
| Slow 🕛       | Fast 🕔        | 120    |  120.03 | C3     | C3, +1ct   |      ~100% |
| Normal 🕛     | Slow 🕛        | 120    |   99.52 | C3     | A2, -25ct  |   82.9333% |
| Normal 🕛     | Normal 🕛      | 120    |  119.92 | C3     | C3, -2ct   |      ~100% |
| Normal 🕛     | Fast 🕔        | 120    |  146.08 | C3     | D#3, -39ct |  121.7333% |
| Fast 🕔       | Slow 🕛        | 120    |  120.16 | C3     | C3, -2ct   |      ~100% |
| Fast 🕔       | Normal 🕖      | 120    |  144.68 | C3     | D#3, +24ct |  120.5666% |
| Fast 🕔       | Fast 🕔        | 120    |  168.22 | C3     | F#3, +13ct |  140.1833% |
