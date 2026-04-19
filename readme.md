# Spike Web Workers with Filesystem Protocol

A simple test to see how Web Workers work (or don't) when loaded from the filesystem and thus use the `file://` protocol. 

Right-click, Save As (computer) / "Share" (iOS): [web-worker-filesystem-spike.html](https://raw.githubusercontent.com/colinkershaw/web-worker-filesystem-spike/refs/heads/main/web-worker-filesystem-spike.html)

## Result

Web Workers seem to work just fine from the `file://` protocol in Chrome and Edge on Windows 11, and also Chrome and Edge on iOS (so WebKit, which should also cover Safari, but it wasn't an option to open the file from Files app) .

## Rationale

Could not get a conclusive answer from searching (internet or AI) if web workers would function with `file://` protocol. An experiment provides a conclusive answer.
