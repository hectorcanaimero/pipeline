# CI/CD Pipeline
Aprender a usar **Pipeline y Github Actions**

## Actions
on: [push]
```
jobs:
  upload_files:
    runs-on: ubuntu-latest
    name: Upload a builded file.
    steps:
    - name: Checkout
      uses: actions/checkout@v2.3.4
    - name: Upload Files
      id: upload
      uses: Creepios/sftp-action@v1.0.1
      with:
        host: ''
        port: 2299
        username: 'root'
        password: ''
        localPath: './'
        remotePath: '/var/www/html/'
```