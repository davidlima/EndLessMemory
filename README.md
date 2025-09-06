# EndLessMemory
IA Multimodal que aprende , almacena y optimiza la memoria para recordar a largo plazo con el objetivo de empatizar cada vez más y más con la persona con la que interactua
# EndLessMemory - Sistema de IA Multimodal

![EndLessMemory Logo](prototipo0.jpg)

Sistema avanzado de IA multimodal que procesa entradas de voz, genera respuestas contextuales y aprende continuamente de cada interacción. Combina modelos de lenguaje grandes (LLMs) con recuperación aumentada de generación (RAG) y fine-tuning mediante LoRA para crear una experiencia conversacional enriquecida y ética.

## 🚀 Características Principales

- **Procesamiento multimodal**: Entrada de voz y salida de texto y voz
- **Memoria infinita**: Sistema RAG que aprende de cada interacción
- **Arquitectura modular**: Múltiples LLMs especializados en diferentes tareas
- **Fine-tuning eficiente**: Implementación de LoRA para adaptación especializada
- **Control ético**: Orquestador con normas éticas y prompts de control
- **Aprendizaje continuo**: Ciclo de retroalimentación constante

## 📊 Diagrama del Sistema

![Diagrama del Sistema EndLessMemory](diagrama.png)

**Diagrama de flujo del proceso**:
```mermaid
flowchart TD
    subgraph Fase1["Fase 1: Proceso Inicial"]
        T["Texto"]
        ASR["ASR"]
        LLMA["LLM-A"]
    end
    subgraph Fase2["Fase 2: Consulta Contextualizada"]
        LLMB["LLM-B"]
        RAG[("Embedding RAG")]
    end
    subgraph Fase3["Fase 3: Integración+Fine-tuning"]
        LLMC["LLM-C + LoRA"]
        O["Orquestador<br>Prompt Ético/Normas"]
    end
    V["Entrada de Voz"] --> ASR
    ASR --> T
    T --> LLMA & LLMB
    RAG <-.-> LLMB & LLMC
    LLMB --> LLMA
    O --> LLMC
    LLMC --> LLMB
    LLMA --> RAG & TTS["TTS<br>Salida de Voz"]
    
    class V,O,ASR input;
    class LLMA,LLMB,LLMC llm;
    class RAG rag;
    class TTS output;
    
    classDef input fill:#fce4ec,stroke:#c2185b,stroke-width:2px;
    classDef output fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px;
    classDef rag fill:#fff3e0,stroke:#ff6f00,stroke-width:2px;
    classDef llm fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px;
