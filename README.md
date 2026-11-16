# cobol-dotnet-interop

An architectural laboratory repository within the **[ortiz-cobol-labs](https://github.com/ortiz-cobol-labs)** organization, designed to explore and demonstrate interoperability patterns between legacy **COBOL** batch/transactional routines and modern **.NET (C#)** applications.

The goal of this project is to implement robust integration strategies for gradual mainframe modernization (*Strangler Fig Pattern*), enabling C# microservices to consume, execute, and exchange data with COBOL systems reliably.

---

## 🎯 Integration Patterns Explored

- **File-Based Batch Pipelines:** Structured data exchange using standardized fixed-length record formats and binary datasets (`COMP`, `COMP-3`) parsed by .NET models.
- **IPC & Native Interop (P/Invoke / C-Bridge):** Direct execution of compiled COBOL shared libraries (`.so` / `.dll`) from C# via native interop.
- **Event-Driven Messaging & Queues:** Decoupled asynchronous integration using messaging patterns (simulating IBM MQ / RabbitMQ workflows) between COBOL producers/consumers and .NET services.
- **REST / gRPC Wrapper API:** Encapuslating legacy COBOL business logic inside modern C# web APIs to expose core functionality to modern clients.

---

## 🏗️ Repository Architecture

```text
.
├── cobol/        # Legacy COBOL routines and copybook structures (.cbl, .cpy)
├── dotnet/       # Modern C# (.NET Core) APIs, services, and binary parsers
├── data/         # Sample input/output datasets and fixed-width files
├── docs/         # Architectural blueprints and integration benchmarks
└── Makefile      # Unified build script for COBOL modules and .NET solution

```

---

## 🚀 Getting Started

### Prerequisites

* **GNUCobol** (`cobc`) for compiling COBOL shared libraries.
* **.NET SDK** (8.0 or later) for building C# services.
* **Make** for build orchestration.

```bash
# Ubuntu / Debian
sudo apt update
sudo apt install open-cobol build-essential dotnet-sdk-8.0

```

### Build & Run

1. **Clone the repository:**
```bash
git clone [https://github.com/ortiz-cobol-labs/cobol-dotnet-interop.git](https://github.com/ortiz-cobol-labs/cobol-dotnet-interop.git)
cd cobol-dotnet-interop

```


2. **Compile COBOL modules and build .NET solution:**
```bash
make build

```


3. **Run the integration pipeline:**
```bash
make run

```


4. **Clean artifacts:**
```bash
make clean

```



---

## 👨‍💻 Maintainer

**Ortiz David**

*Senior Software Engineer & Systems Architect*

[GitHub Profile](https://github.com/ortizdavid) • [Portfolio](https://www.google.com/search?q=https://ortizdavid.github.io)

