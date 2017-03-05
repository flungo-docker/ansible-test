# Ansible Test

Docker image for testing ansible roles. Ansible is run as a non-root user with passwordless sudo priviledges.

To use, create a Dockerfile containing the following:

```
FROM flungo/ansible-test:archlinux
```

On build, this image copies the contents of the build directory into `/usr/src/ansible` before running the test playbook contained at `test/main.yml`.
