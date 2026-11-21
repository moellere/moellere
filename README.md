<!-- DRAFT for review. Not published. Paste into moellere/moellere/README.md when you're happy with it. -->

# Hi, I'm Enoch 👋

I've spent my career running data center infrastructure, and at home I run a small one on purpose: a Proxmox and Talos/Kubernetes homelab managed through GitOps, a house full of ESPHome devices, a few 3D printers, and a growing list of robots.

Most of what's here comes from one idea: **automation that does the tedious work and asks before it acts.** Several of these projects share a "trust gradient," where reads and proposals are automatic and anything that changes the world waits for a human tap. A lot of it is built in close collaboration with Claude, and the repos say so.

## 🛠️ Featured projects

**[WireStudio](https://github.com/moellere/WireStudio)** · Hardware design tool for ESP32 / ESP8266 devices
One `design.json` drives everything: solved pin assignments, electrical validation (boot-strap pins, ADC2 vs Wi-Fi, voltage rails), firmware for seven frameworks (ESPHome, Tasmota, WLED, LoRaWAN, Meshtastic, CircuitPython, MicroPython), a KiCad schematic and PCB, a JLCPCB fab bundle and a parametric OpenSCAD enclosure. Web UI, built-in agent, MCP server, and WebSerial flashing, including to a remote bench. Shared designs live in [wirestudio-designs](https://github.com/moellere/wirestudio-designs), where CI validates every submission the same way the studio does.

**[homelab-helper](https://github.com/moellere/homelab-helper)** · Inventory, audit and operator-gated execution for homelabs
Discovers what you run across Proxmox, Kubernetes, Talos, NetBox, UniFi, MikroTik, Cloudflare, Argo CD, Home Assistant and more; reconciles it against kernel ground truth; and recommends placement, rightsizing and fixes. Predicts disk failures and capacity exhaustion from history. Read-only by default; execution sits behind a deterministic trust gradient that no LLM is ever in the path of. Chat and MCP tools included.

**[print-warden](https://github.com/moellere/print-warden)** · Klipper print staging and monitoring
Hand off everything after design: headless OrcaSlicer slicing, gcode staging, start-on-phone-tap, and monitoring from Moonraker telemetry, Obico failure detection and cameras. It classifies Klipper shutdowns, watches fans and runout sensors, plans the week's queue, and exposes an MCP server.

**[lorawan-for-esphome](https://github.com/moellere/lorawan-for-esphome)** · LoRaWAN MAC component for ESPHome
ESPHome ships LoRa radio drivers but no LoRaWAN stack. This adds OTAA join and uplinks from any ESPHome sensor, built on RadioLib. Hardware-tested on SX1262 and SX1276 boards with session resume, deep sleep and Class C downlinks.

**[Grover (rover)](https://github.com/moellere/rover)** · A tracked workbench rover learning to look after itself
A Makeblock tank with an ESP32-S3 "spinal cord" and an off-board brain. It docks and charges itself using an overhead camera, gyro and visual homing, and keeps a dated journal of who decided what, human or Claude.

## 🔌 ESPHome and Home Assistant

- **[esphome-vivo-desk](https://github.com/moellere/esphome-vivo-desk)**: transparent serial interposer for VIVO standing desks. Height and presets in Home Assistant while the handset keeps working. Also includes an under-desk bike conversion.
- **[hass-google-weather-maps](https://github.com/moellere/hass-google-weather-maps)**: Home Assistant integration that turns Google's weather map tiles into a radar-style camera entity.
- **[awningcontrol](https://github.com/moellere/awningcontrol)**: the one that started it, a retractable awning driven by a cordless drill and a Wemos D1 Mini.

## ☸️ Kubernetes and network tooling

- **[uptime-kuma-reconciler](https://github.com/moellere/uptime-kuma-reconciler)**: controller that creates Uptime Kuma monitors from Ingress, Gateway API, Traefik and Istio resources, plus static ping and port monitors.
- **[guacamole-reconciler](https://github.com/moellere/guacamole-reconciler)**: declarative Apache Guacamole connections from YAML, GitOps style.
- **[unifi-dns-sync](https://github.com/moellere/unifi-dns-sync)**: keeps DNS records consistent across multiple UniFi controllers. (Experimental, and the README means it.)

## 🤝 Contributions and forks

Forks of tools I build on, several carrying my own changes: [kubernetes-opnsense-controller](https://github.com/moellere/kubernetes-opnsense-controller) and its [Helm chart](https://github.com/moellere/kubernetes-opnsense-controller-chart) (plugin support), [Embedded-AI-Harness](https://github.com/moellere/Embedded-AI-Harness), [fleet-for-esphome](https://github.com/moellere/fleet-for-esphome), [ProxmoxMCP-Plus](https://github.com/moellere/ProxmoxMCP-Plus) and [ardupilot](https://github.com/moellere/ardupilot).

<!-- OPTIONAL: private work. Delete this section if you'd rather not mention any of it. -->
## 🔒 Also building (private for now)

- An AI-piloted, solar-recharged survey boat on ArduPilot, with LoRaWAN telemetry and a full digital twin so the software is finished before the hull is.
- A self-hosted family meal-planning app.
- A git-backed "second brain" that all my AI agents read from, with a curator workflow for changes.
- The GitOps repo behind my Talos cluster, plus Terraform and Ansible for the rest of the lab.

## 🧰 Toolbox

Python · C++ (ESP32) · Kubernetes · Talos · Argo CD · Helm · Proxmox · Terraform · Ansible · ESPHome · Home Assistant · Klipper / Moonraker · LoRaWAN / ChirpStack · KiCad · OpenSCAD · MCP
