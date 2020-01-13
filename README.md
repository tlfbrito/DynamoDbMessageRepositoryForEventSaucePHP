# DynamoDB Message Repository for EventSauce

This library is an implementation of a DynamoDB Repository for PHP [EventSauce](https://eventsauce.io/).

This implementation as all the features similar to
[Doctrine Message Repository](https://github.com/EventSaucePHP/DoctrineMessageRepository).
(official supported by [EventSauce](https://eventsauce.io/)) but for AWS DynamoDB.

### Usage:
```php
<?php

namespace App\Repository;

use Brito\DynamoDbMessageRepository;

class MyCustomRepository extends DynamoDbMessageRepository {

}

```
#### Register your Repository (Symfony)

```yaml
    App\Repository\MyCustomRepository:
        arguments:
            - '@aws.dynamodb'
            - '@EventSauce\EventSourcing\Serialization\ConstructingMessageSerializer'
            - 'event-source-table-name'
```

### Tests

```bash
$ cd tests && docker-compose up

$ phpunit tests/
