Turning the DB inside-out with Apache Samza
===========================================

Martin Kleppma
@martkinkl
[Samza website](http://samza.incubator.apache.org)

## Typical web app
 - Browser/client app (stateless)
 - Backend (stateless)
 - DB (mutable global state)

## Derived Data
- Repliction
- Secondary index
- Caching
    + Cache in application is difficult
- Materialized view: copy the data into a temp table.

## Samza
- Take the idea of materialized view for caching
- Take replication stream from implementation detail into public interface.
- Materialized view from the stream
- Kappa architecture (as opposed to lambda architecture)

### Better data
- for analytic it's better to keep the stream of data, for example in shopping cart, better to keep track if item is removed from cart.

### Fully precomputed caches
no cold cache/warnming, no race condition

Clients subscribe to materials views.
- Request/response
- Subscribe/notify
    + Meteor, Firebase
- **Stream everywhere**