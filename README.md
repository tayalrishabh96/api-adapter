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

- manifest/adapter-credentials.yaml
