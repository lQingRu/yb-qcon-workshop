# Resilience
- Readily respond or recover from change, disruption or a crisis
- Technical, Operational, Financial

## Design patterns
- Circuit breaker pattern
  - Prevent cascading failures by temporarily blocking requests to a failing component
- Retry pattern
  - Automatically retry failed operations to handle transient features
- Bulkhead pattern
  - Isolate components to prevent failures in one area from affecting others

## Principles of resilient design
- Redundancy
  - Ensure availability
- Failover
  - Automatically switch to backup systems
- Load balancing
  - Prevent overload
- Isolation
  - Prevent failures from spreading

# Distributed SQL database
- Transactionally consistent on multiple servers
  - Scales vertically by adding more CPUs AND scales horizontally by adding more nodes

## Yugabyte
- Pluggable query layer
  - YSQL API (postgres compatible)
  - YCQL API (Based on CQL)
  - Other APIs (future)
- Distributed, transactional storage layer
  - Automatic sharding
  - Load balancing
  - Distributed transactions
  - [Raft consensus](https://raft.github.io/)
    - Typically is odd number
    - Writes will hurt if too many replications (eg. 9)
- Deploy anywhere
- https://github.com/akscjo/yb-qcon-workshop