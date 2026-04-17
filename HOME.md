# 🧠 Cérebro do Bruno

> *"O objetivo não é acumular notas — é construir uma rede de pensamentos que gere novos insights."*

---

## 🗺️ Mapas de Conteúdo

| Área | Mapa |
|------|------|
| Engenharia de Software | [[MOC - Engenharia de Software]] |
| Arquitetura de Sistemas | [[MOC - Arquitetura de Sistemas]] |
| Inteligência Artificial | [[MOC - IA e ML]] |
| Projetos Ativos | [[MOC - Projetos]] |
| Aprendizado Contínuo | [[MOC - Aprendizado]] |

---

## 📥 Fluxo de Trabalho

```
Captura (Inbox) → Ideia (02) → Nota de Literatura (03) → Nota Permanente (04)
```

1. **Capturar** → Jogue tudo em `[[00_INBOX]]`, sem pensar
2. **Processar** → Transforme em ideia em `02_IDEIAS`
3. **Referenciar** → Notas de livros/cursos em `03_NOTAS_LITERATURA`
4. **Sintetizar** → Seu próprio pensamento em `04_NOTAS_PERMANENTES`

---

## 📊 Estatísticas do Cofre

```dataview
TABLE length(file.inlinks) as "Links Recebidos", length(file.outlinks) as "Links Enviados"
FROM ""
SORT length(file.inlinks) DESC
LIMIT 10
```

---

## 📅 Notas Recentes

```dataview
TABLE file.ctime as "Criada em"
FROM ""
SORT file.ctime DESC
LIMIT 8
```

---

#home #índice
