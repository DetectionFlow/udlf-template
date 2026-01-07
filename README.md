# UDLF Detections Repository

This repository contains detection rules in [Universal Detection Lifecycle Format (UDLF)](https://github.com/DetectionFlow/udlf-schema).

## Structure

```
├── udlf-schema.json          # JSON Schema for UDLF validation (from udlf-schema repo)
└── detections/
    ├── endpoint/             # Endpoint detection rules
    ├── network/              # Network detection rules
    ├── application/          # Application/identity detection rules
    └── other/                # Other detection rules
└── hunting/                  # UDLF files for hunting queries
└── detection-strategies/     # Detection strategy UDLF yaml
└── deployments/              # Deploymet UDLF yaml
```

## UDLF Format

Each detection is stored as a YAML file with the `.udlf.yaml` extension. Files include a yaml-language-server directive for VS Code validation:

```yaml
# yaml-language-server: $schema=../../udlf-schema.json
id: "uuid"
title: "Detection Name"
format: "udlf"
lifecycle: "deployed"
type: "ttp"
# ...
```

## Schema

The UDLF schema is maintained at [DetectionFlow/udlf-schema](https://github.com/DetectionFlow/udlf-schema).
