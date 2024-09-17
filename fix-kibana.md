# Lấy Enrollment Token

```sh
docker exec elasticsearch /usr/share/elasticsearch/bin/elasticsearch-create-enrollment-token -s kibana
```

## To check the file permissions and ensure `kibana.yml` is writable by the Kibana process in Docker, you can follow these steps:

### 1. Run the command as `root` inside the container:

```sh
docker exec -it --user root kibana /bin/bash
```

### 2. Change the permissions of the `kibana.yml` file as `root`:

```sh
cd /usr/share/kibana/config
```

```sh
chmod 664 kibana.yml
```

```sh
chown kibana:kibana kibana.yml
```

### 3. Verify the permissions: After changing the permissions or ownership, you can verify them with the ls -l command:

```sh
ls -l kibana.yml
```

### 4. Exit the container:

```sh
exit
```

### 5. Restart the Kibana container: After making the changes, you may need to restart the Kibana container:

```sh
docker restart kibana
```


# Default user

**Username**: `elastic`

**Password**: The password is generated automatically during the initial setup of Elasticsearch.

## To retrieve the password for `elastic`:

### **If security is enabled and you forgot the password**: You can reset the password by using the following command inside the Elasticsearch container:

```sh
docker exec -it elasticsearch /usr/share/elasticsearch/bin/elasticsearch-reset-password -u elastic
```
