# CHANGELOG

## [0.1.0] - 2026-05-29

### Added

- Journal — 日记账实体（id, name, createdAt）
- JournalEntry — 凭证实体（id, journalId, createdAt, description, lines）
- JournalEntryLine — 分录行（id, type, amount, description, createdAt），支持多行
- LineType 枚举（debit / credit）
- 基于 freezed 的不可变模型，支持 copyWith 与 JSON 序列化
