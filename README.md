# vips-contracts
Visma Idella BV public resources, OpenAPI and other SCHEMA specifications

👤 [Visma Idella][info@visma-idella.nl]

This repository contains the data contracts for the VIPS product lines. It serves as the source of truth for the public-facing APIs and events, structured by product line.

## 📖 Introduction

This repository is the central location for all data contracts related to the VIPS product lines. It is designed to be the single source of truth that drives consistency across our services. The repository is organized by product line, with each line containing its own set of `json-schemas`, `open-api`, and `cloudevents` definitions.

### Repository Structure

The repository is organized by product line, starting with `pensions`. Each product line folder contains subfolders for the different types of contracts:
```
/
└── pensions/
    ├── json-schemas/
    │   ├── generic/
    │   │   └── name-of-the-entity/
    │   │       └── 1.0.0/
    │   │           ├── name-of-the-entity.schema.json
    │   │           └── name-of-the-entity.example.json
    │   └── microservice-a/
    │       └── name-of-the-entity/
    │           └── 1.0.0/
    │               ├── name-of-the-entity.schema.json
    │               └── name-of-the-entity.example.json
    ├── open-api/
    │   └── name-of-the-api/
    │       └── v1.0/
    │       │   └── name-of-the-api.oas.yaml
    │       └── v1.1/
    │       │   └── name-of-the-api.oas.yaml
    │       └── v2.0/
    │           └── name-of-the-api.oas.yaml    
    └── cloudevents/
        ├── internal-events/
        │   └── group-name/
        │       └── v1.0/
        │       │   └── entity-name-data.schema.json
        │       │   └── entity-name-data.simple-example.json
        │       │   └── entity-name-data.complex-example.json
        │       └── v1.1/
        │       │   └── entity-name-data.schema.json
        │       │   └── entity-name-data.simple-example.json
        │       └── v2.0/
        │           └── entity-name-data.schema.json
        │           └── entity-name-data.simple-example.json
        │           └── entity-name-data.complex-example.json
        └── external-events/
            └── external-group-name/
                └── v1.0/
                    └── entity-name-data.schema.json
                    └── entity-name-data.simple-example.json
                    └── entity-name-data.complex-example.json
    
```

### Standards

All contracts within this repository adhere to the following standards:

* **File and Folder Naming**: All file and folder names use `kebab-case`.
* **JSON Schema Properties**: Properties are written in `lower_snake_case`.
* **Enums**: Enum values are written in `UPPER_SNAKE_CASE`.
* **OpenAPI Version**: All `open-api` specifications are written in OAS 3.1.
* **JSON Schema Versioning**: For `json-schemas`, each entity has its own folder. Inside, a subfolder for each semantic version (e.g., `1.0.0`) contains the `name-of-the-entity.schema.json` and a corresponding `name-of-the-entity.example.json` file.
* **Grouping of JSON Schemas**: json-schemas are grouped based on the microservice that is the source of truth for them

