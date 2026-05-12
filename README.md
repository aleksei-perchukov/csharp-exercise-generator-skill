# Coding Exercise Coaches — Claude Code Marketplace

Маркетплейс из 9 плагинов-тренеров для Claude Code: упражнения, проверки решений и дозированные подсказки по C#, Go, Java, JavaScript, Kotlin, Python, Rust, Swift и TypeScript. Весь вывод — только на русском языке.

## Список плагинов

| Язык | Имя плагина | Префикс команд |
|---|---|---|
| C# | `csharp-exercise-generator-skill` | `/csharp-exercise-*` |
| Go | `go-exercise-generator-skill` | `/go-exercise-*` |
| Java | `java-exercise-generator-skill` | `/java-exercise-*` |
| JavaScript | `javascript-exercise-generator-skill` | `/js-exercise-*` |
| Kotlin | `kotlin-exercise-generator-skill` | `/kotlin-exercise-*` |
| Python | `python-exercise-generator-skill` | `/python-exercise-*` |
| Rust | `rust-exercise-generator-skill` | `/rust-exercise-*` |
| Swift | `swift-exercise-generator-skill` | `/swift-exercise-*` |
| TypeScript | `typescript-exercise-generator-skill` | `/ts-exercise-*` |

## Установка

Из Claude Code добавьте маркетплейс одной командой:

```
/plugin marketplace add aleksei-perchukov/coding-exercise-generator-ide-plugin
```

Затем установите нужный плагин (по одному или несколько):

```
/plugin install csharp-exercise-generator-skill@aperchukov-skills
/plugin install go-exercise-generator-skill@aperchukov-skills
/plugin install java-exercise-generator-skill@aperchukov-skills
/plugin install javascript-exercise-generator-skill@aperchukov-skills
/plugin install kotlin-exercise-generator-skill@aperchukov-skills
/plugin install python-exercise-generator-skill@aperchukov-skills
/plugin install rust-exercise-generator-skill@aperchukov-skills
/plugin install swift-exercise-generator-skill@aperchukov-skills
/plugin install typescript-exercise-generator-skill@aperchukov-skills
```

Рекомендуется использовать последний Claude Sonnet с Extended Thinking.

## Команды (одинаковы для всех плагинов)

Подставьте префикс языка вместо `<prefix>` (например, `python`, `java`, `js`, `ts`, `kotlin`, `csharp`, `go`, `rust`, `swift`).

| Команда | Описание |
|---|---|
| `/<prefix>-exercise-new` | Новое упражнение по выбранному языку |
| `/<prefix>-exercise-pattern` | Упражнение по паттернам проектирования или принципам SOLID |
| `/<prefix>-exercise-hint` | Следующая подсказка (5 уровней, от намёка до почти-решения) |
| `/<prefix>-exercise-check` | Проверка кода: только ✅ или ❌, без объяснений |
| `/<prefix>-exercise-fix` | Исправление кода с объяснениями и мнемотехникой |
| `/<prefix>-exercise-clear` | Создать рабочий проект с заготовкой для упражнения |

## Как работает сессия

1. Выбери команду (`/<prefix>-exercise-new` или `/<prefix>-exercise-pattern`).
2. Укажи сложность от 1 до 10.
3. Выбери тему из меню.
4. Получи упражнение и реши его в редакторе.
5. Запусти `/<prefix>-exercise-check`, чтобы узнать результат.
6. Если застрял — `/<prefix>-exercise-hint` (до 5 раз), затем `/<prefix>-exercise-fix`.

## Темы упражнений по языкам

### C#
**Основы C#** — условия, циклы, вещественные числа, массивы, методы, строки, константы/структуры/enum/switch, кортежи, локальные функции, NRT, исключения, даты/время/таймзоны, лямбда-выражения.

**ООП** — классы, конструкторы, свойства, наследование, полиморфизм, абстракция, интерфейсы, record/DTO/with.

**Коллекции и LINQ** — generics, интерфейсы коллекций, List/Dictionary/HashSet, индексаторы, Extension Members, компараторы, LINQ-запросы, группировка, агрегатные функции, объединения и проекции.

**Файлы, Streams, сериализация** — файловая система, кодировки, обработка ошибок, FileStream, BufferedStream, StreamReader/StreamWriter, сериализация JSON и XML.

**Асинхронность и многопоточность** — многопоточность, синхронизация потоков, потокобезопасные коллекции, Task/async/await/ValueTask, отмена, Parallel.For, потоки данных, генераторы, Channel, SynchronizationContext, события.

**Рефлексия, логгирование, память** — рефлексия, динамические типы, logging/мониторинг/трассировка, устройство памяти в .NET.

**Паттерны (GoF)** — Singleton, Factory, Builder, Adapter, Decorator, Strategy, Observer, Command и другие.
**SOLID** — все пять принципов с практическими примерами.

### Go
**Основы Go** — условия/switch/type switch, циклы/range, типы данных, массивы/слайсы, функции (multiple return/variadic), строки/[]byte/[]rune, карты, указатели, константы/iota, обработка ошибок (error/errors.Is/errors.As/%w), defer/panic/recover, даты/время.

**Структуры и интерфейсы** — структуры/теги, методы (value/pointer receiver), встраивание/композиция, интерфейсы (неявная реализация), any/type assertion, стандартные интерфейсы, generics.

**Коллекции и обработка данных** — slices/maps packages, sort, closures, io.Reader/io.Writer, regexp, range-over-func (Go 1.23).

**Файлы, I/O и сериализация** — os, bufio, filepath, encoding/json, XML/CSV, fmt.

**Конкурентность** — горутины, каналы, select, sync (WaitGroup/Mutex/RWMutex/Once), sync/atomic, context, паттерны (fan-in/fan-out/pipeline/worker pool), errgroup.

**Продвинутые темы** — тестирование (table-driven/benchmarks), рефлексия, unsafe/cgo, build tags, go generate, профилирование/pprof.

**Паттерны** — Singleton (sync.Once), Factory Function, Builder, Functional Options, Adapter, Middleware, Strategy, Observer, Pipeline, Worker Pool и другие.

**SOLID** — все пять принципов адаптированы для Go (через интерфейсы и композицию).

### Java
**Основы Java** — условия, циклы, примитивные типы/обёртки/autoboxing, массивы, методы, строки/StringBuilder, enum/switch expressions, varargs/var, даты/время/таймзоны, исключения/try-with-resources, лямбды/функциональные интерфейсы, Optional.

**ООП** — классы, конструкторы, инкапсуляция, record/sealed classes, наследование, полиморфизм, абстрактные классы, интерфейсы с default/static методами, вложенные/анонимные классы.

**Коллекции и Stream API** — generics/wildcards, List/Set/Map/Queue/Deque, Comparable/Comparator, Collections, Stream API (filter/map/flatMap/reduce/collect/groupingBy, parallel streams).

**Файлы, I/O, сериализация** — File/Path/Files, InputStream/OutputStream/Reader/Writer, буферизация, Serializable, JSON (Jackson/Gson), XML (JAXB), NIO.2, кодировки.

**Многопоточность и асинхронность** — Thread/Runnable/synchronized/volatile, ExecutorService/ThreadPool/Future, CompletableFuture, Lock/Semaphore/CountDownLatch, ConcurrentHashMap/BlockingQueue, Virtual Threads.

**Рефлексия, аннотации и продвинутые темы** — рефлексия, аннотации, logging (SLF4J/Logback), модульная система, управление памятью и GC.

**Паттерны (GoF)** — Singleton, Factory, Builder, Adapter, Decorator, Strategy, Observer, Command и другие.

**SOLID** — все пять принципов с практическими примерами.

### JavaScript
**Основы JavaScript** — условия/switch/nullish coalescing, циклы (for/for...of/for...in), типы данных, массивы/spread/деструктуризация, функции (declaration/expression/arrow/rest), строки/template literals, объекты (shorthand/computed/optional chaining), приведение типов, обработка ошибок, даты, замыкания, регулярные выражения.

**Функции и контексты** — var/let/const (hoisting/TDZ), замыкания (IIFE/мемоизация/каррирование), this (default/implicit/explicit/new/arrow), call/apply/bind, прототипы, итераторы, генераторы, WeakRef.

**ООП** — классы (constructor/методы/поля), наследование (extends/super), инкапсуляция (# private), static, миксины, Proxy/Reflect, Symbol.

**Коллекции и функциональное программирование** — Array methods, Map/Set/WeakMap/WeakSet, Object methods, каррирование, иммутабельность, pipe/compose, JSON.

**Асинхронность** — callbacks, промисы, async/await, Promise.all/allSettled/race/any, AsyncIterator, AbortController, event loop, Web Workers.

**Модули и продвинутые темы** — ES Modules, CommonJS vs ESM, structuredClone, Intl, ArrayBuffer/TypedArrays, Proxy/Reflect/Symbol, дескрипторы свойств.

**Паттерны** — Singleton, Factory, Builder, Prototype, Decorator, Strategy, Observer (EventEmitter/CustomEvent), Iterator, Middleware, Module, Pub/Sub, Mixin и другие.

**SOLID** — все пять принципов с практическими примерами.

### Kotlin
**Основы Kotlin** — if/else и when как выражение, циклы/ranges, типы данных, массивы/списки, функции (default/named arguments, Unit, Nothing), строки/string templates, null safety, enum classes, обработка ошибок (runCatching/Result), даты/время, лямбды/SAM, деструктуризация.

**ООП** — классы (primary/secondary constructors), свойства (val/var, lateinit), data classes/copy, sealed classes, наследование (open/override/abstract), интерфейсы, object/companion object, visibility, delegation (by, lazy, observable).

**Коллекции и функциональное программирование** — List/Set/Map (mutable/immutable), map/filter/flatMap/groupBy/zip/fold, Sequences, scope functions (let/run/with/apply/also), extension functions, inline/reified, generics (in/out variance).

**Файлы, I/O и сериализация** — File, java.nio.file.Path, kotlinx.serialization, Jackson/Gson, use (try-with-resources).

**Конкурентность и корутины** — launch/async/runBlocking, suspend, Dispatchers, structured concurrency, Flow, Channels, SharedFlow/StateFlow, CoroutineExceptionHandler.

**Продвинутые темы** — DSL-строители, contracts/smart casts, рефлексия, аннотации, мультиплатформа (expect/actual), context receivers/value classes.

**Паттерны (GoF)** — Singleton (object), Factory (companion object/sealed class), Builder/DSL builder, Prototype, Decorator (delegation by), Strategy, Observer (Flow/StateFlow), State (sealed class) и другие.

**SOLID** — все пять принципов с практическими примерами.

### Python
**Основы Python** — условия, циклы, числа/Decimal, списки, кортежи, функции, строки/f-strings, словари, множества, распаковка/*args/**kwargs, аннотации типов, исключения, даты/время/таймзоны, лямбды, генераторы и итераторы.

**ООП** — классы, __init__, @property, dataclasses, NamedTuple, наследование/MRO, полиморфизм/duck typing, ABC, typing.Protocol, магические методы.


**Коллекции и функциональное программирование** — defaultdict, Counter, deque, comprehensions, итераторы, map/filter/reduce, сортировка/компараторы, itertools, functools.

**Файлы, сериализация** — open/with, pathlib, CSV, JSON, pickle, YAML, кодировки, обработка ошибок ввода-вывода.

**Асинхронность и многопоточность** — threading, Lock, GIL, multiprocessing, Pool, asyncio, async/await, Task, gather, асинхронные генераторы и контекстные менеджеры.

**Метапрограммирование и продвинутые темы** — декораторы, контекстные менеджеры, метаклассы, дескрипторы, logging/отладка.

**Паттерны (GoF)** — Singleton, Factory, Builder, Adapter, Decorator, Strategy, Observer, Command и другие.

**SOLID** — все пять принципов с практическими примерами.

### Rust
**Основы Rust** — if/else и match как выражения, циклы, типы данных, Vec/массивы/слайсы, функции, строки (String vs &str, UTF-8), кортежи/деструктуризация, enum (Option/Result), обработка ошибок (?/unwrap/map/and_then), замыкания (Fn/FnMut/FnOnce/move), pattern matching.

**Ownership и типы** — ownership/move/Copy, borrowing (&T/&mut T), lifetimes, структуры, traits (default methods/trait bounds), trait objects (dyn Trait) vs generics, generics (where/associated types), deriving traits, smart pointers (Box/Rc/Arc/RefCell/Cow).

**Коллекции и итераторы** — Vec, HashMap/BTreeMap (entry API), HashSet/BTreeSet, Iterator trait, адаптеры (map/filter/flat_map/zip/chain), потребители (collect/fold/reduce), custom Iterator impl.

**Файлы, I/O и сериализация** — std::fs, BufReader/BufWriter, std::path, serde (Serialize/Deserialize/serde_json), Display/Debug, thiserror/anyhow.

**Конкурентность** — std::thread, mpsc-каналы, Mutex/RwLock/Arc, atomic types, rayon (par_iter), async/await (Future/tokio).

**Продвинутые темы** — макросы (macro_rules!), unsafe Rust (FFI), HRTB, type state pattern, модули/видимость, тестирование (#[test]/integration tests), error handling паттерны.

**Паттерны** — Builder (идиоматический), Factory (new/from/with_), Newtype, Type State, Adapter/Decorator (через трейты), Strategy, Observer, Iterator, RAII/Drop, Interior mutability (RefCell/Cell), Cow<T>, Extension trait.

**SOLID** — все пять принципов адаптированы для Rust (через трейты, generics и композицию).

### Swift
**Основы Swift** — условия/guard/switch с pattern matching, циклы/stride, типы данных, массивы/кортежи, функции/inout/variadic, строки/Unicode/String.Index/Substring, словари/множества, optionals, enum (associated/raw values, indirect), обработка ошибок/Result, замыкания/@escaping, даты.

**ООП и типы** — struct vs class (value vs reference), свойства (stored/computed/lazy/observers), методы, инициализаторы (designated/convenience/failable), наследование/override/final, протоколы/protocol extensions/composition, расширения/conditional conformance, generics, access control, ARC/weak/unowned.

**Коллекции и функциональное программирование** — Array/Set/Dictionary, Sequence/Collection/IteratorProtocol, map/filter/reduce/flatMap/compactMap, lazy sequences, Comparable, key paths/KVO, Slice/ArraySlice/Substring, zip/enumerated/stride.

**Файлы, кодирование и сериализация** — FileManager/URL/Data, Codable/CodingKeys, JSONEncoder/JSONDecoder, PropertyListEncoder/Decoder, кодировки.

**Асинхронность и многопоточность** — GCD (DispatchQueue/DispatchGroup), async/await/Task/TaskGroup, structured concurrency (async let, cancellation), actors/Sendable, AsyncSequence/AsyncStream, MainActor.

**Продвинутые темы** — opaque types (some)/existential types (any), result builders (@resultBuilder), property wrappers (@propertyWrapper), macros, pattern matching, ARC/retain cycles.

**Паттерны (GoF)** — Singleton, Factory, Builder, Adapter, Decorator, Strategy, Observer, Command и другие.

**SOLID** — все пять принципов с практическими примерами.

### TypeScript
**Основы TypeScript** — условия, циклы, примитивные типы, массивы/кортежи/readonly, функции/перегрузки, строки/шаблонные литералы, объекты/деструктуризация, enum, даты, исключения, стрелочные функции/замыкания, промисы/async/await.

**Система типов** — type aliases/interfaces, union/intersection, literal types/const assertions, type narrowing/type guards, generics (constraints, default types), utility types (Partial/Pick/Omit/Record/ReturnType), mapped/conditional types, template literal types, discriminated unions.

**ООП** — классы, конструкторы/parameter properties, модификаторы доступа, наследование/implements, абстрактные классы, полиморфизм, миксины, декораторы.

**Коллекции и функциональное программирование** — Array methods, Map/Set/WeakMap/WeakSet, итераторы/генераторы, каррирование, иммутабельность (readonly/as const), discriminated unions, pipe/compose, Record<K,V>/индексные типы.

**Асинхронность** — промисы, async/await, Promise.all/allSettled/race/any, AsyncIterator/for await...of, AbortController, event loop.

**Модули, тестирование и продвинутые темы** — ES Modules, declaration files (.d.ts), Result/Either паттерн, branded types, infer/рекурсивные типы, типизация сторонних библиотек/DefinitelyTyped.

**Паттерны (GoF)** — Singleton, Factory, Builder, Adapter, Decorator, Strategy, Observer, Command и другие.

**SOLID** — все пять принципов с практическими примерами.

## Требования

| Плагин | Требования для команды `*-exercise-clear` |
|---|---|
| C# | .NET 8.0 или выше; JetBrains Rider или любой редактор с терминалом |
| Go | Go 1.22 или выше; JetBrains GoLand или VS Code с Go extension |
| Java | Java 17 или выше; JetBrains IntelliJ IDEA или любой редактор с терминалом |
| JavaScript | Node.js 18+; JetBrains WebStorm, VS Code или любой редактор с терминалом |
| Kotlin | Kotlin 1.9 или выше; JetBrains IntelliJ IDEA или любой редактор с терминалом |
| Python | Python 3.10 или выше; JetBrains PyCharm или любой редактор с терминалом |
| Rust | Rust (edition 2021+) и Cargo; JetBrains RustRover, VS Code с rust-analyzer или любой редактор с терминалом |
| Swift | Swift 5.9 или выше; Xcode или любой редактор с терминалом |
| TypeScript | Node.js 18+ и TypeScript 5.0+; JetBrains WebStorm или VS Code с терминалом |

Общие требования для всех плагинов:
- Claude Code с поддержкой slash-команд
- Рекомендуется последний Claude Sonnet с Extended Thinking

## Структура репозитория

```
.
├── .gitignore
├── README.md
├── .claude-plugin/
│   └── marketplace.json         # манифест маркетплейса (9 плагинов)
└── plugins/
    ├── csharp/
    ├── go/
    ├── java/
    ├── javascript/
    ├── kotlin/
    ├── python/
    ├── rust/
    ├── swift/
    └── typescript/
        ├── .claude-plugin/plugin.json
        ├── .claude/commands/*.md
        └── skills/<lang>-exercise-generator-skill/SKILL.md
```

## Лицензия

MIT