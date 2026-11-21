- **An edit reaching a chain of wildcard imports re-expands the chain once.** Expansion now purges
  every importer down the chain in one round and derives them upstream first, instead of purging and
  deriving the chain again one link per round; an incremental `ParseSources` edit of the Apollo 11
  model drops from about 1.8 s to 0.8 s at p95, with byte-identical responses.
