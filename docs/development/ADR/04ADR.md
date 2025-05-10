## Architecture Decision Record (ADR) - Post Creation Refactor

- Post yaratımında userID ayrıca istenmesine gerek yok. Kullanıcı zaten oturum ile jwt token gönderiyor.

 ### Validation

  - Zod validasyonu gereksiz olabilir zira GQL'de zaten validasyon yapılıyor. Ancak, Zod validasyonu, GraphQL'den bağımsız olarak kullanılabilir ve bu nedenle yararlı olabilir.

