# Services - Simple Quere Service - Components
- Messages:
  - Each message can contain up to 256KB of text (in any format)
  - It guarantees delivery of each message at least once but does not guarantee the order (best effort) in which they are delivered to the queue, and duplicates can occur.
  - They are stored in the queue for up to 14 days