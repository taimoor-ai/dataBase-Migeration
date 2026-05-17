### What exactly is a migration?

Think of your database like a city's infrastructure. When the city was first built, the roads, buildings, and pipes were laid out in a certain way. As the city grows, you need to add new roads, widen old ones, or demolish outdated buildings. You cannot do this randomly — you need a **controlled, versioned plan** so that every worker knows what changed, when, and in what order.

A **database migration** is exactly that — a versioned, ordered script that changes your database schema (or data) in a controlled, repeatable, and reversible way.


#### Simple mental model

**Migration = Git commit, but for your database structure.**

Just like Git tracks every code change, migrations track every database change. Every team member applies the same migrations in the same order, and every environment (dev, staging, production) ends up with an identical schema.




# Migration Lifecycle

Developer writes migration file
        ↓
Git push
        ↓
CI/CD runs migration
        ↓
Staging DB updated
        ↓
Production DB updated
        ↓
Other devs run same migration locally
