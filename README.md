# dumps
Storage for Database dumps that can be useful for development or presentation of the project

# Usage
Clone [scripts for docker](https://github.com/rimelek/scripts-for-docker) into the same parent folder of the annotation project

```
├── annotation  (or any other root folder name)
│   ├── api
│   ├── frontend
│   ├── setup
│   ├── pipeline
│   ├── difference-calc
│   ├── dumps
│   ├── difference-calc
├── scripts-for-docker
  ```

### Create dump
```bash
cd ../../scripts-for-docker
```

```
./bin/docker-volume-export.sh annotation_data ../annotation/dumps/<own-dump-name>.tgz
```

### Import dump
```bash
cd ../../scripts-for-docker
```

```
./bin/docker-volume-import.sh ../annotation/dumps/<dump-name>.tgz annotation_data
```
