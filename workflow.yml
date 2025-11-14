name: Deploy Hyperswitch App
run-name: Hyperswitch App ${{ inputs.environment }} Deployment - Tag ${{ inputs.version_tag }}

on:
  workflow_dispatch:
    inputs:
      environment:
        description: 'Choose environment'
        required: true
        type: choice
        options:
        - 'integ'
        - 'sandbox'
        default: 'integ'
      version_tag:
        description: 'Version Tag'
        required: true
        type: string

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:

      - name: Install yq
        run: |
          sudo wget -qO /usr/local/bin/yq https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64
          sudo chmod +x /usr/local/bin/yq

