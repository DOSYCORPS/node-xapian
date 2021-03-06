# node-xapian
xapian bindings for node using n-api

# Requirements
You must have `xapian-core` installed.

# Docs / Classes
- Database
    - `Database()`
    - `Database(path: string, flags = 0)`
    - `close()`
    - `reopen()` -> `bool`
    - `.size` / `get_size()` -> `number`
    - `get_description()` -> `string`
    - `has_positions()` -> `bool`
    - `.doccount` / `get_doccount()` -> `number`
    - `.lastdocid` / `get_lastdocid()` -> `number`
    - `get_avlength()` -> `number`
    - `get_total_length()` -> `number`
    - `get_doclength(docid: number)` -> `number`
    - `get_document(docid: number)` -> `Document`
    - `get_metadata(key: string)` -> `string`
    - `get_uuid()` -> `string`
    - `locked()` -> `bool`
    - `get_revision()` -> `number`
    - `compact(path: string, flags=0, block_size=0)`
- WritableDatabase
    - all of the fields and methods from `Database`
    - `WritableDatabase()`
    - `WritableDatabase(path: string, flags=0)`
    - `commit()`
    - `begin_transaction()` / `begin_transaction(val: boolean)`
    - `commit_transaction()`
    - `cancel_transaction()`
    - `add_document(doc: Document)` -> `docid (number)`
    - `delete_document(docid: number)` / `delete_document(bool_term: string)`
    - `replace_document(docid: number, doc: Document)` / `replace_document(bool_term: string, doc: Document)` -> `docid`
    - `add_spelling(spelling: string)` / `add_spelling(spelling: string, n: number)`
    - `remove_spelling(spelling: string)` / `remove_spelling(spelling: string, n: number)`
    - `add_synonym(word1: string, word2: string)`
    - `remove_synonym(word1: string, word2: string)`
    - `clear_synonyms()`
    - `set_metadata(key: string, value: string)`
- Document
    - `Document()`
    - `get_value(slot: number)` -> `string`
    - `add_value(slot: number, value: string)` -> `string`
    - `remove_value(slot: number)`
    - `clear_values()`
    - `.data` / `get_data()` -> `string`
    - `.data` / `set_data(data: string)`
- Enquire
- MSet
- MSetIterator
- QueryParser
- Query
- Stem
- TermGenerator
- TermIterator

