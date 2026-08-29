## Introduction

This document is a companion collection of GitHub projects associated with the review. It brings together publicly available code, datasets, models, prompts, and experimental platforms from previous studies in large-language-model-assisted framework-materials research. These repositories represent the accumulated knowledge and practical contributions of the community.

The organization follows Chapters 3–7 of the review. Projects are included when a paper explicitly provides them in its Data Availability, Code Availability, Supporting Information, or main text. Public web applications, online demos, and model-hub deployments mentioned by the source papers are also recorded, even when they are not GitHub repositories. General-purpose packages cited only as dependencies are listed separately in Appendix A.

The same project may appear in more than one chapter when it supports multiple stages of the framework-materials research workflow. Links have been normalized to remove common line-break, spacing, capitalization, and trailing-slash inconsistencies.

## Chapter 3. Cross-cutting Benchmarks and Evaluation Challenges

This chapter covers evaluation of LLM reliability, framework-materials knowledge, knowledge-graph question answering, structure representation, and structure validation.

| Project                                         | Function                                                     | Source                                     | Link                                                         |
| ----------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------ | ------------------------------------------------------------ |
| Evaluation of open-source LLMs for MOF research | Evaluates open-source LLMs on chemistry, MOF knowledge, information extraction, research assistance, and paper polishing | `J. Chem. Inf. Model. 2024, 64, 4958–4965` | [GitHub](https://github.com/MontageBai/Evaluation-of-open-source-large-language-models-for-metal-organic-frameworks-research) |
| KGQA4MAT                                        | MOF knowledge-graph question answering data, MOF-KG definitions, prompts, and evaluation code | `arXiv:2309.11361`                         | [GitHub](https://github.com/kgqa4mat/KGQA4MAT)               |
| MOF2Text                                        | Textual representations of MOF structures and related validation models | `arXiv:2608.11283`                         | [GitHub](https://github.com/sxm13/MOF2Text)                  |
| MOFClassifier2                                  | Text-based MOF classification and structural-reasonableness validation | `arXiv:2608.11283`                         | [GitHub](https://github.com/sxm13/MOFClassifier2)            |

## Chapter 4. Text and Multimodal Mining

This chapter covers extraction of synthesis conditions, entity and relation recognition, knowledge-graph construction, chemical text modelling, and the organization of information from papers, supporting materials, and databases.

| Project                             | Function                                                     | Source                                     | Link                                                         |
| ----------------------------------- | ------------------------------------------------------------ | ------------------------------------------ | ------------------------------------------------------------ |
| MOF synthesis-condition extraction  | Extracts MOF synthesis conditions and performs data processing and property inference | `J. Chem. Inf. Model. 2026, 66, 228–245`   | [Repository](https://github.com/BHT321/MOFs_Synthesis_Condition_Extraction) |
| CSD-MOF extraction dataset          | Dataset directory for extracted synthesis conditions and related data | `J. Chem. Inf. Model. 2026, 66, 228–245`   | [Dataset](https://github.com/BHT321/MOFs_Synthesis_Condition_Extraction/tree/main/Dataset) |
| CSD-MOF extraction code             | LLM-based synthesis extraction and density/surface-area inference code | `J. Chem. Inf. Model. 2026, 66, 228–245`   | [Code](https://github.com/BHT321/MOFs_Synthesis_Condition_Extraction/tree/main/Code) |
| MOFs synthesis-condition extraction | GPT-based implementation reported in the paper; the source text contains a line-break artifact | `J. Chem. Inf. Model. 2026, 66, 228–245`   | [Candidate repository](https://github.com/passingby000/MOFs_Synthesis_Condition_Extraction) |
| NERRE                               | Scientific entity and relation extraction, including data, preprocessing, training, and evaluation | `Nature Communications 2024, 15, 1418`     | [GitHub](https://github.com/LBNLP/NERRE)                     |
| NERRE-Llama                         | Llama-2 fine-tuning, inference code, and weight-download scripts | `Nature Communications 2024, 15, 1418`     | [GitHub](https://github.com/lbnlp/nerre-llama)               |
| SFTLLMs for ChemText Mining         | Supervised fine-tuning and evaluation for chemical text mining | `Chemical Science 2024, 15, 10600–10611`   | [GitHub](https://github.com/zw-SIMM/SFTLLMs_for_ChemText_Mining) |
| KGFM                                | Framework-materials knowledge-graph construction, question set, and Neo4j resources | `npj Computational Materials 2025, 11, 51` | [GitHub](https://github.com/MontageBai/KGFM)                 |
| MOF_ChemUnity                       | MOF names, coreference relations, and water-stability labels | `J. Am. Chem. Soc. 2025, 147, 43474–43486` | [GitHub](https://github.com/AI4ChemS/MOF_ChemUnity)          |
| GPT-MOF Project                     | ChatGPT-based mining of MOF synthesis and CO2-capture information | `Digital Discovery 2026, 5, 384–396`       | [GitHub](https://github.com/ai4mat-lab/GPT_MOF_Project)      |
| LLMs-GPT-4-Cage                     | Text classification, information tabularization, and a runnable chatbot for POCs/COFs | `Digital Discovery 2025, 4, 403–410`       | [GitHub](https://github.com/syy1213/LLMs-GPT-4-Cage)         |
| spbnet                              | Data preprocessing, pretraining, and fine-tuning for materials/chemical text modelling | `Nature Communications 2026, 17, 2618`     | [GitHub](https://github.com/tyvanzou/spbnet)                 |

### Public applications and model-hub resources

| Application or resource                             | Function                                                     | Source                                   | Link                                                         | Status                                                       |
| --------------------------------------------------- | ------------------------------------------------------------ | ---------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| MaterialBrain online engine                         | Online engine for literature-grounded MOF synthesis extraction, structure inference, and synthesis guidance | `J. Chem. Inf. Model. 2026, 66, 228–245` | [Web application](https://materialbrain.com)                 | Public demo explicitly reported by the paper                 |
| MOF synthesis extraction online engine and database | Online executable engine and database for the large-scale synthesis data produced in the study | `J. Chem. Inf. Model. 2026, 66, 228–245` | Not specified in the paper                                   | Application explicitly mentioned; no stable public URL was provided |
| TWA–Marie web demo                                  | Natural-language and field-based access to zeolite and crystallographic knowledge through the The World Avatar knowledge graph | `Digital Discovery 2024, 3, 2070–2081`   | [Web demo](https://theworldavatar.io/demos/marie/)           | Public web interface explicitly reported by the paper        |
| BERT-base-uncased                                   | Retrieval encoder used for few-shot example selection in the MaterialBrain workflow | `J. Chem. Inf. Model. 2026, 66, 228–245` | [Hugging Face model](https://huggingface.co/google-bert/bert-base-uncased) | Supporting model, not an author-developed application        |
| all-MiniLM-L6-v2                                    | Sentence-embedding model used for retrieval in the MaterialBrain workflow | `J. Chem. Inf. Model. 2026, 66, 228–245` | [Hugging Face model](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2) | Supporting model, not an author-developed application        |

## Chapter 5. Experiment Assistance and Human–AI Collaboration

This chapter covers experiment design, linker modification, rule discovery, property screening, PXRD analysis, framework synthesis, and scale-up. The projects retain human judgement and experimental validation as essential parts of the workflow.

| Project                                            | Function                                                     | Source                                                     | Link                                                         |
| -------------------------------------------------- | ------------------------------------------------------------ | ---------------------------------------------------------- | ------------------------------------------------------------ |
| ChatGPT-Lab                                        | ChatGPT-assisted experiment design, Bayesian optimization, and data analysis | `ACS Central Science 2023, 9, 2161–2170`                   | [GitHub](https://github.com/zach-zhiling-zheng/ChatGPT-Lab)  |
| Linker-Mutation                                    | MOF linker mutation, prompts, fine-tuned models, and data    | `J. Am. Chem. Soc. 2023, 145, 28284–28295`                 | [GitHub](https://github.com/zach-zhiling-zheng/Linker-Mutation) |
| Chemist-Guided Human-AI Workflow for COF Synthesis | Chemist-led human–AI workflow with scripts, prompts, configurations, and examples | `J. Am. Chem. Soc. 2026, 148, 7440–7449`                   | [GitHub](https://github.com/Hans-12138/Chemist-Guided-Human-AI-Workflow-for-Covalent-Organic-Framework-Synthesis) |
| Fine-tuned-Gemini                                  | Fine-tuning experiments for chemical representations and linker-related tasks | `J. Mater. Chem. A 2025, 13, 19307–19315`                  | [GitHub](https://github.com/xiaoyu961031/Fine-tuned-Gemini)  |
| FluoroCOFs                                         | COF design and iterative experimental recommendation         | `Nature Chemistry 2025, 17, 1645`                          | [GitHub](https://github.com/pic-ai-robotic-chemistry/Fluorocofs) |
| MOF-Scaleup                                        | Structured reaction parameters and support for MOF scale-up  | `arXiv:2604.20899`                                         | [GitHub](https://github.com/zzhenglab/MOF-Scaleup)           |
| Multi-objective MOF screening                      | Multi-objective screening for CO2 capture and conversion     | `Separation and Purification Technology 2025, 376, 133939` | [GitHub](https://github.com/MontageBai/Multi-Objective-Screening-of-MOFs-with-An-Integrated-AI-System-for-CO2-Capture-and-Conversion) |
| C5 quinary-mixture screening                       | Data-driven MOF discovery for C5 quinary-mixture separation  | `J. Am. Chem. Soc. 2025, 147, 42016–42023`                 | [GitHub](https://github.com/MontageBai/Data-driven-discovery-of-metal-organic-frameworks-for-sieving-separation-of-C5-quinary-mixture-) |
| Reasoning Language Model as Rule Finder            | Discovers and extracts interpretable rules from materials data | `J. Mater. Chem. A 2025, 13, 19307–19315`                  | [GitHub](https://github.com/Wang-Group/Reasoning-Language-Model-as-Rule-Finder) |
| pxrdif-generator                                   | PXRD simulation/generation and structure-analysis assistance | `J. Am. Chem. Soc. 2026, 148, 10094–10104`                 | [GitHub](https://github.com/nakulrampal/pxrdif-generator)    |

## Chapter 6. Agent Systems: Orchestrating Tools, Databases, and Models

This chapter focuses on task decomposition, tool selection, state management, database and knowledge-graph access, simulation, and traceable workflow execution.

| Project                        | Function                                                     | Source                                                 | Link                                                         |
| ------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------------ |
| ChatMOF                        | Conversational LLM tools and knowledge access for MOF research | `Nature Communications 2024, 15, 4705`                 | [GitHub](https://github.com/Yeonghun1675/ChatMOF)            |
| DynaMate                       | Multi-agent molecular-dynamics input generation, execution, and analysis | `Molecular Systems Design & Engineering 2025, 10, 585` | [GitHub](https://github.com/omendibleba/DynaMate)            |
| SciToolAgent                   | LLM agent for scientific-tool use                            | `arXiv:2507.20280`                                     | [GitHub](https://github.com/hicai-zju/scitoolagent)          |
| Ara                            | COF fragment screening, search, and optimization workflow    | `arXiv:2603.05188`                                     | [GitHub](https://github.com/Iman-Peivaste/Ara)               |
| ElAgenteGrafico-ChatTranscript | Chat transcripts and workflow resources for a graphical agent | `arXiv:2602.17902`                                     | [GitHub](https://github.com/jb2197/ElAgenteGrafico-ChatTranscript) |
| ChemGraph                      | Graph-based tools and agent infrastructure for science and materials research | `arXiv:2604.07681`                                     | [GitHub](https://github.com/argonne-lcf/ChemGraph)           |
| XpertAI                        | AI/agent tools for scientific research tasks                 | `Communications Chemistry 2025, 8, 11`                 | [GitHub](https://github.com/geemi725/XpertAI)                |
| LLM4MOF                        | LLM tools for MOF research                                   | `arXiv:2606.29459`                                     | [GitHub](https://github.com/kn1218/LLM4MOF)                  |
| ChemReasoner-Code              | Code and resources for a chemistry reasoning model           | `Digital Discovery 2026, 5, 869–877`                   | [GitHub](https://github.com/MontageBai/ChemReasoner-Code)    |
| Conversational LLM AI Agent    | Conversational agent and customized research code            | `ACS Nano 2025, 19, 23840–23858`                       | [GitHub](https://github.com/tuantuan-lin/A-Conversational-Large-Language-Model-AI-Agent) |
| Eunomia                        | Natural-language interaction and tool calling for chemical discovery | `Digital Discovery 2024, 3, 2607–2617`                 | [GitHub](https://github.com/AI4ChemS/Eunomia)                |
| MOFh6                          | Framework-materials agent and knowledge-processing project   | `Transactions of Materials Research 2026, 2, 100176`   | [GitHub](https://github.com/lzhzzzzwill/MOFh6)               |

### Public deployments and related portals

| Application or resource    | Function                                                     | Source                                               | Link                                                         | Status                                            |
| -------------------------- | ------------------------------------------------------------ | ---------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------- |
| MOFh6 Hugging Face Space   | Browser-accessible deployment of the MOFh6 dialogue, structure-visualization, and CIF-service application | `Transactions of Materials Research 2026, 2, 100176` | [Hugging Face Space](https://huggingface.co/spaces/Willlzh/MOFh6) | Space deployment explicitly reported by the paper |
| MOFGen public project page | Public Materials Project page containing the MOFGen database, DFT calculations, and structure-visualization resources | `arXiv:2504.14110`                                   | [Materials Project](https://next-gen.materialsproject.org/contribs/projects/MOFGen) | Public portal explicitly reported by the source   |

### Framework-materials tools

| Tool             | Function                                              | Source                                                       | Link                                                    |
| ---------------- | ----------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------- |
| MOFseek          | MOF ligand/structure recognition and annotation       | `Angew. Chem. Int. Ed. 2026, 65, e13366`                     | [GitHub](https://github.com/DanielEss-lab/MOFseek)      |
| MOFid            | MOF structure identification and decomposition        | `Angew. Chem. Int. Ed. 2026, 65, e13366`                     | [GitHub](https://github.com/snurrgroup/mofid)           |
| MOFs-LLM         | MOF-related language-model project                    | `Angew. Chem. Int. Ed. 2026, 65, e13366`                     | [GitHub](https://github.com/cgarls/MOFs-LLM)            |
| MOFTransformer   | MOF property-prediction baseline                      | `J. Am. Chem. Soc. 2025, 147, 3943–3958`                     | [GitHub](https://github.com/hspark1212/MOFTransformer)  |
| L2M3             | Materials text-mining and materials-modelling project | `J. Am. Chem. Soc. 2025, 147, 3943–3958`; `Digital Discovery 2026, 5, 1981–1990` | [GitHub](https://github.com/Yeonghun1675/L2M3)          |
| L2M3_ML          | Machine-learning models accompanying L2M3             | `J. Am. Chem. Soc. 2025, 147, 3943–3958`                     | [GitHub](https://github.com/Taeun8991/L2M3_ML)          |
| L2M3_application | Application code for L2M3                             | `J. Am. Chem. Soc. 2025, 147, 3943–3958`                     | [GitHub](https://github.com/Taeun8991/L2M3_application) |

## Chapter 7. Automated and Closed-loop Experiments

This chapter covers the transition from model recommendations to real or semi-automated experiments, in which experimental outcomes update the model, screening strategy, or next-round conditions.

| Project                 | Function                                                     | Source                                     | Link                                                         |
| ----------------------- | ------------------------------------------------------------ | ------------------------------------------ | ------------------------------------------------------------ |
| ChemicalExplorerCopilot | Natural-language/LLM interface for an automated chemistry platform | `J. Am. Chem. Soc. 2025, 147, 23014–23025` | [GitHub](https://github.com/Wang-Group/ChemicalExplorerCopilot) |
| FluoroCOFs              | Robotic experiments and iterative COF optimization           | `Nature Chemistry 2025, 17, 1645`          | [GitHub](https://github.com/pic-ai-robotic-chemistry/Fluorocofs) |
| ChatGPT-Lab             | LLM-assisted experiment design and Bayesian-optimization loop | `ACS Central Science 2023, 9, 2161–2170`   | [GitHub](https://github.com/zach-zhiling-zheng/ChatGPT-Lab)  |
| MOF-Scaleup             | Reaction-condition structuring and scale-up support          | `arXiv:2604.20899`                         | [GitHub](https://github.com/zzhenglab/MOF-Scaleup)           |
| TCP-IP-4Axis-Python     | Dobot MG400 robotic-arm control interface                    | `J. Am. Chem. Soc. 2025, 147, 23014–23025` | [GitHub](https://github.com/Dobot-Arm/TCP-IP-4Axis-Python)   |
| Commanduino             | Instrument-control framework used in automated experiments   | `J. Am. Chem. Soc. 2025, 147, 23014–23025` | [GitHub](https://github.com/croningp/commanduino)            |

### Public application deployments

| Application or resource     | Function                                                     | Source                                               | Link                                                         | Status                                             |
| --------------------------- | ------------------------------------------------------------ | ---------------------------------------------------- | ------------------------------------------------------------ | -------------------------------------------------- |
| MOFh6 Hugging Face Space    | Deployed interface for natural-language MOF queries, CIF retrieval, and structure visualization | `Transactions of Materials Research 2026, 2, 100176` | [Hugging Face Space](https://huggingface.co/spaces/Willlzh/MOFh6) | Public deployment explicitly reported by the paper |
| MaterialBrain online engine | Online interface connecting literature mining, structure inference, Bayesian optimization, and synthesis guidance | `J. Chem. Inf. Model. 2026, 66, 228–245`             | [Web application](https://materialbrain.com)                 | Public demo explicitly reported by the paper       |

# This project is continuously being updated....
