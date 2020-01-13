# DynamoDB Message Repository for EventSauce

This library is an implementation of a DynamoDB Repository for PHP [EventSauce](https://eventsauce.io/).

This implementation as all the features similar to
[Doctrine Message Repository](https://github.com/EventSaucePHP/DoctrineMessageRepository).
(official supported by [EventSauce](https://eventsauce.io/)) but for AWS DynamoDB.

### Tests

```bash
$ cd tests && docker-compose up

$ phpunit tests/
