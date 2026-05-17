### What exactly is a migration?

Think of your database like a city's infrastructure. When the city was first built, the roads, buildings, and pipes were laid out in a certain way. As the city grows, you need to add new roads, widen old ones, or demolish outdated buildings. You cannot do this randomly — you need a **controlled, versioned plan** so that every worker knows what changed, when, and in what order.

A **database migration** is exactly that — a versioned, ordered script that changes your database schema (or data) in a controlled, repeatable, and reversible way.


#### Simple mental model

**Migration = Git commit, but for your database structure.**

Just like Git tracks every code change, migrations track every database change. Every team member applies the same migrations in the same order, and every environment (dev, staging, production) ends up with an identical schema.




# Migration Lifecycle

<pre class="overflow-visible! px-0!" data-start="3169" data-end="3349"><div class="relative w-full mt-4 mb-1"><div class=""><div class="relative"><div class="h-full min-h-0 min-w-0"><div class="h-full min-h-0 min-w-0"><div class="border border-token-border-light border-radius-3xl corner-superellipse/1.1 rounded-3xl"><div class="h-full w-full border-radius-3xl bg-token-bg-elevated-secondary corner-superellipse/1.1 overflow-clip rounded-3xl lxnfua_clipPathFallback"><div class="pointer-events-none absolute end-1.5 top-1 z-2 md:end-2 md:top-1"></div><div class="relative"><div class="pe-11 pt-3"><div class="relative z-0 flex max-w-full"><div id="code-block-viewer" dir="ltr" class="q9tKkq_viewer cm-editor z-10 light:cm-light dark:cm-light flex h-full w-full flex-col items-stretch ͼs ͼ16"><div class="cm-scroller"><pre class="cm-content q9tKkq_readonly m-0"><code><span>Developer creates migration</span><br/><span>        ↓</span><br/><span>Migration stored in Git</span><br/><span>        ↓</span><br/><span>CI/CD executes migration</span><br/><span>        ↓</span><br/><span>Migration recorded in DB</span><br/><span>        ↓</span><br/><span>Application uses new schema</span></code></pre></div></div></div></div></div></div></div></div></div></div></div></div></pre>
