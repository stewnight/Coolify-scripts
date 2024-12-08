---
title: 'Backups'
head:
  - tag: 'meta'
    attrs:
      property: 'og:title'
      content: 'How to configure database backups in Coolify'
description: 'A guide how backups work in Coolify.'
---

import { Aside } from '@astrojs/starlight/components';

Scheduled database backups can be configured for Databases and for the Coolify PostgreSQL database itself.

These schedules are based on cron expressions, so you can configure them to run as often as you want. For more information about cron expressions, see our [cron syntax](/docs/knowledge-base/cron-syntax) documentation.

## PostgreSQL

Coolify creates a full backup of your PostgreSQL databases. You can specify which database to backup, with a comma separated list.

<Aside type="tip">Coolify's own database is also backed up using this method.</Aside>

### Backup command

```bash
pg_dump --format=custom --no-acl --no-owner --username <username> <databaseName>
```

### Restore command

The backup has custom format, so you can restore it using the following command (or with any equivalent tool):

```bash
pg_restore --verbose --clean -h localhost -U postgres -d postgres pg-dump-postgres-1697207547.dmp
```

## MySQL

```bash
mysqldump -u root -p <password> <datatabaseName>
```

## MariaDB

```bash
mariadb-dump -u root -p <password> <datatabaseName>
```

## MongoDB

```bash
mongodump --authenticationDatabase=admin --uri=<uri> --gzip --archive=<archive>
```

Or if you exclude some collections:

```bash
mongodump --authenticationDatabase=admin --uri=<uri> --gzip --archive=<archive> --excludeCollection=<collectionName> --excludeCollection=<collectionName>
```

## S3 Backups

You can also define your own [S3 compatible](/docs/knowledge-base/s3) storage to store your backups.
