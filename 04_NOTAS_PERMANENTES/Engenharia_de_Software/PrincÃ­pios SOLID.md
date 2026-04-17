---
titulo: Princípios SOLID
criado: 2025-01-01
tags: [permanente, engenharia-de-software, boas-praticas]
status: maduro
---

# Princípios SOLID

## 💡 Ideia Central

> SOLID é um conjunto de 5 princípios que tornam o código orientado a objetos mais fácil de manter, estender e testar.

---

## 🧠 Desenvolvimento

### S — Single Responsibility
Cada classe deve ter **uma única razão para mudar**. Se uma classe faz autenticação *e* envia e-mail, ela tem duas responsabilidades — divida-a.

### O — Open/Closed
Entidades devem ser **abertas para extensão, fechadas para modificação**. Use herança ou composição para adicionar comportamento, não edite código existente.

### L — Liskov Substitution
**Subtipos devem ser substituíveis** pelos seus tipos base sem quebrar o programa. Se `Pato` herda de `Ave` mas não pode voar, a hierarquia está errada.

### I — Interface Segregation
**Interfaces finas** são melhores que interfaces gordas. Clientes não devem depender de métodos que não usam.

### D — Dependency Inversion
**Dependa de abstrações, não de implementações concretas.** Módulos de alto nível não devem depender de módulos de baixo nível — ambos devem depender de interfaces.

---

## 🔗 Conexões

- Relacionado com: [[Clean Code — principais conceitos]]
- Relacionado com: [[Design Patterns — visão geral]]
- Relacionado com: [[Arquitetura Hexagonal]]

---

## 📚 Fontes

- Robert C. Martin, *Clean Architecture* (2017)

#permanente #solid #engenharia-de-software
