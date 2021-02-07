```bash
workspace: /root
```

Directory where downloaded files will be temporarily stored.

```bash
sonar_download_validate_certs: true
```

Controls whether to validate certificates when downloading SonarQube.

```bash
sonar_download_url: http://dist.sonar.codehaus.org/sonarqube-4.5.4.zip
sonar_version_directory: sonarqube-4.5.4
```

The URL from which SonarQube will be downloaded, and the resulting directory name (should match the download archive, without the archive extension).

```bash
sonar_web_context: ''
```

The value of sonar.web.context. Setting this to something like /sonar allows you to set the context where Sonar can be accessed (e.g. hostname/sonar instead of hostname).

Using the defaults, you can view the SonarQube home at http://localhost:9000/ (default System administrator credentials are admin/admin).

```bash
sonar_mysql_username: sonar
sonar_mysql_password: sonar

sonar_mysql_host: localhost
sonar_mysql_port: "3306"
sonar_mysql_database: sonar

sonar_mysql_allowed_hosts:
  - 127.0.0.1
  - ::1
  - localhost
```

  JDBC settings for a connection to a MySQL database. Defaults presume the database resides on localhost and is only accessible on the SonarQube server itself.

Run playbook 

```bash
ansible-playbook playbook-sonar.yaml -i inventroy.txt
```
