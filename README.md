# Potree GPU Point Cloud Offline Test Package

This repository contains an offline Potree point-cloud test package for GPU validation on Hygon + Kylin Linux desktops.

## Artifact

- `potree-gpu-test.zip`

The zip includes:

- Potree 1.8.2 static viewer files.
- Synthetic transmission-line-style point clouds at 5M, 10M, and 20M points.
- Test pages for each point budget.
- Kylin Linux run instructions.
- CSV result template.

## Run On Test Machine

```bash
unzip potree-gpu-test.zip
cd potree-gpu-test
chmod +x start-server.sh
./start-server.sh 8080
```

Open:

```text
http://localhost:8080/tests/test-20m.html
```

Before recording results, check `chrome://gpu` and confirm WebGL/WebGL2 are hardware accelerated, not SwiftShader.

## Scope

This package tests point-cloud rendering only. BIM/triangle-mesh workloads should be tested separately with a mesh/BIM viewer or benchmark.
