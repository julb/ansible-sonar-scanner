# sonar-scanner

This role enables to install [SonarScanner](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner/) on a system.

Prior to the installation of the Sonar-Scanner, the playbook will install `java-11-openjdk`.
Then, it will install the sonar-scanner package free of the embedded JVM.

## Requirements

No requirements.

## Role Variables

| Name                                  | Type     | Location            | Description                                                                                                                       |
| ------------------------------------- | -------- | ------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| sonar_scanner_version                 | string   | `defaults/main.yml` | The version of sonar-scanner to install. Defaults to `4.6.2.2472`.                                                                |
| sonar_scanner_releases_url            | string   | `defaults/main.yml` | The base URL of sonar_scanner releases repository. Defaults to `https://binaries.sonarsource.com/Distribution/sonar-scanner-cli`. |
| sonar_scanner_package_sha256_checksum | string   | `defaults/main.yml` | The SHA256 checksum of the sonar-scanner package. Defaults to `344bfeff44b09a11082b4a4646b1ed14f213feb00a5cd6d01c86f3767cb32471`. |
| sonar_scanner_global_properties       | string{} | `defaults/main.yml` | A dictionary listing all properties to set in the sonar-scanner.properties file. Defaults to `{}`.                                |
| sonar_scanner_executable              | string   | `vars/main.yml`     | The local path where to install sonar-scanner package. Defaults to `/opt/sonar-scanner`.                                          |
| sonar_scanner_installation_folder     | string   | `vars/main.yml`     | The local path where to install sonar-scanner executable. Defaults to `/usr/local/sbin/sonar-scanner`.                            |

## Dependencies

No dependencies.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
    - { role: julb.sonar_scanner }
```

## License

MIT

## Author Information

More to find on my [Github](https://github.com/julb).

## Contributing

This project is totally open source and contributors are welcome.

When you submit a PR, please ensure that the syntax has been checked.
