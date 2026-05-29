# 量潮财务管理Dart工具箱

## Models

- **Journal** — 日记账（id, name, createdAt）
- **JournalEntry** — 凭证（id, journalId, createdAt, description, lines）
- **JournalEntryLine** — 分录行（id, type, amount, description, createdAt）

## Usage

```dart
import 'package:quanttide_finance/quanttide_finance.dart';

final journal = Journal(id: '1', name: '备用金', createdAt: DateTime.now());

final entry = JournalEntry(
  id: 'je1', journalId: journal.id, createdAt: DateTime.now(),
  description: '购买办公用品',
  lines: [
    JournalEntryLine(id: 'l1', type: LineType.debit, amount: 1200),
    JournalEntryLine(id: 'l2', type: LineType.credit, amount: 1200),
  ],
);
```

## License

Apache 2.0
