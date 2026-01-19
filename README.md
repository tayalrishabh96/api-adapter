# API Adapter

A lightweight **API Adapter framework** built using Python.
This project implements the **Adapter Design Pattern** to trigger heal job in devtron and repond to tacker with a specific status code.

---

## 📌 Problem Statement

When integrating tacker directly with heal job, it fails due to tacker's limitation of expecting a specific status code HTTP 204 and hence api adaptor is acting as proxy in between :
- responds back to tacker with status code HTTP 204 
- Uses authentication mechanisms as required by Tacker

This adaptor is tightly coupled with what is required by Tacker.

---

## 🗂 Variables that need to be configured as per cluster and heal job :

- manifest/adapter-configmap.yaml
  - devtron_url : devtron's URL for example - https://devtron.example.com
  - ciPipelineId : CI Pipeline ID corresponding to heal job
  - ciPipelineMaterialsId : CI Pipeline's Material ID corresponding to heal job
  - GitCommitId : Github Commit ID corresponding to heal job
- manifest/adapter-credentials.yaml
  - devtron_api_token : devtron api token with permissions to be able to trigger devtron heal job 
