# 📝 LivingDoc – The Living Documentation Framework for Python  



[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)  
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)  
[![Living Documentation](https://img.shields.io/badge/living--documentation-enabled-green)](#)  

🚀 **LivingDoc** is a Python framework, _under construction_, that aims to integrate **architectural annotations, design stereotypes, and project documentation** directly into the source code.  
Inspired by **Living Documentation** principles as **Software Crafters** do, it enables seamless **self-documenting code, guided tours, dependency validation, and AI-assisted development**.  

---

## ✨ Features  

✔ **Embedded Annotations**: Decorators for DDD, architectural patterns, testing, and code smells  
✔ **Project Documentation**: Automatically generate project docs, glossaries, and word clouds  
✔ **Guided Tours**: Annotate key components to improve onboarding and project understanding  
✔ **Dependency Validation**: Ensure design consistency with automated code checks  
✔ **Gherkin & User Stories**: Link features with business needs for better traceability  
✔ **AI-Enhanced Development**: Structure design metadata for future AI-assisted coding  

---

## 📦 Installation  

```sh
pip install livingdoc
```

Or via **Poetry**:

```sh
poetry add livingdoc
```

---

## 🚀 Quick Start  

### 1️⃣ **Annotate Your Code**  

Use LivingDoc’s decorators to enrich your source code with **design intentions**:  

```python
from livingdoc.architecture import Adapter
from livingdoc.ddd import ValueObject

@ValueObject
class Money:
    """Represents a monetary value with a currency."""
    def __init__(self, amount: float, currency: str):
        self.amount = amount
        self.currency = currency

@Adapter
class PaymentGatewayAdapter:
    """Adapts a third-party payment API."""
    def __init__(self, gateway):
        self.gateway = gateway
```

### 2️⃣ **Scan and Extract Documentation**  

Run the LivingDoc CLI to analyze your project:  

```sh
livingdoc scan my_project
```

📌 Example Output:  

```
🔍 Scanning package: my_project
📌 ValueObject: my_project.Money
   📝 Represents a monetary value with a currency.

📌 Adapter: my_project.PaymentGatewayAdapter
   📝 Adapts a third-party payment API.
```

### 3️⃣ **Export as JSON for Automated Documentation**  

```sh
livingdoc scan my_project --format=json --output=documentation.json
```

Use this JSON output to generate **Markdown, HTML, or integrate with your AI tools**.

---

## 🎯 Use Cases  

🔹 **Improve Code Understanding**: Embedded annotations make design explicit  
🔹 **Generate Living Documentation**: Automate documentation directly from code  
🔹 **Facilitate Onboarding**: Guided tours help new developers get up to speed  
🔹 **Ensure Code Consistency**: Validate dependencies and design rules  
🔹 **Enhance AI-powered Development**: Provide structured metadata for AI coding assistants  

---

## 🛠 Supported Annotations  

### 🏗 **Architectural Annotations**  
- `@Adapter` – Marks an adapter pattern implementation  
- `@Repository` – Marks a repository class  
- `@Service` – Identifies a service class  

### 🏛 **Domain-Driven Design (DDD)**  
- `@ValueObject` – Declares a value object  
- `@Entity` – Identifies an entity  
- `@AggregateRoot` – Marks an aggregate root  

### 🎨 **Design Patterns**  
- `@Factory` – Designates a factory pattern  
- `@Singleton` – Identifies a singleton pattern  

### 🚨 **Code Smells & Properties**  
- `@Deprecated` – Marks deprecated code  
- `@Experimental` – Flags experimental features  

### 🎓 **Guided Tour**  
- `@GuidedTour("intro")` – Marks key entry points for project onboarding  

---

## 📖 Roadmap  

✅ **Initial release with core annotations**  
⏳ **Integration with Sphinx for documentation generation**  
⏳ **Automated dependency validation**  
⏳ **Advanced AI-assisted coding tools**  

🚀 **Contribute & Shape the Future of LivingDoc!**  

---

## 🤝 Contributing  

Contributions are welcome! If you have ideas for new annotations or improvements:  

1. Fork the repository  
2. Create a feature branch  
3. Submit a pull request  

---

## 📝 License  

LivingDoc is released under the **MIT License**.  

---

## 📣 Stay Updated  

📢 Follow the project for updates and discussions!  

🚀 Let's turn **source code** into **self-documenting, intelligent software**!  
