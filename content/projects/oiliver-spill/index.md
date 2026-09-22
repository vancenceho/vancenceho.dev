+++
title = 'Oiliver Spill'
date = 2026-09-22T10:53:22+08:00
draft = false
description = "An IoT and cloud system for early oil spill detection along tanker routes, using an ESP32 buoy with infrared sensing and LoRA communication."
summary = "Academic project (SUTD 50.042 Cloud Computing & IoT) building an ESP32-based buoy that detects oil on the water surface via infrared and LoRA, backed by AWS cloud infrastructure for data collection and analysis."
tags = ["iot", "esp32", "lora", "aws", "terraform", "opentofu", "cloud-computing", "python"]
showHero = false
# Add a featured.png / cover.jpg to this page bundle, then set showHero = true
+++

{{< alert icon="circle-info" >}}
Academic project for 50.042 Cloud Computing & IoT - currently released as an MVP with a PoC, however easily scalable with more capital/hardware investment; further improvements could be made and feel free to check it those out in the section below!
{{< /alert >}}

## Overview

Oiliver Spill is a system to help oil companies detect early oil spills along tanker routes - reducing cleanup costs and protecting marine ecosystems from prolonged chemical exposure. A buoy fitted with an ESP32 uses infrared sensing to detect oil on the water surface and transmits readings over LoRA to a cloud backend for collection, storage, and analysis.

## Architecture

- **ESP32 + infrared sensor + LoRA** - on-buoy detection and transmission
- **AWS API Gateway** - ingestion entrypoint for sensor data
- **AWS Lambda** - serverless processing of incoming sensor JSON
- **S3** - raw/cleaned/processed sensor data storage
- **AWS RDS PostgresSQL** - central database for analytics
- **AWS ECS Fargate** - containerised frontend + backend service
- **AWS ALB** - application load balancer for API routes
- **AWS ECR** - container registry for containerised application services
- **Terraform / OpenTofu** - infrastructure as code for provisioning of services

## Tech Stack

- **Python** - backend processing service
- **Terraform / OpenTofu** - IaC for AWS
- **Docker** - containerised microservices
- **Shell / Makefile** - deployment automation

## Links

{{< button href="https://github.com/vancenceho/oiliver-spill" target="_blank" >}}
View on GitHub
{{< /button >}}
