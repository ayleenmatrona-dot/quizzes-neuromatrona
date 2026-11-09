# Suplemento S1. Matriz clínica de regresión: 38 casos

Fuente: 02-clinical-spec-v1.md §23 (1–25), §29 (26–38), con addendum humano. Cada caso valida IDs y completitud del contrato antes de evaluar. Metadata no especificada se responde «no sé»; nunca se agrega evidencia positiva. Datos sintéticos. PASS demuestra regresión técnica, no aprobación clínica.

| Caso fuente | Test | Resultado esperado (ejes, salida, flags) | Estado |
|---|---|---|---|
| 1. A clásico, alta confianza | clinical-38.test.ts → 1 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"positive","confidence":"high"},"types":["A"],"confidence":"high"} | PASS |
| 2. B clásico, alta confianza | clinical-38.test.ts → 2 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"negative","confidence":"high"},"types":["B"],"confidence":"high"} | PASS |
| 3. C clásico, alta confianza | clinical-38.test.ts → 3 | {"od":{"state":"negative","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"positive","confidence":"high"},"types":["C"],"confidence":"high"} | PASS |
| 4. D clásico, alta confianza | clinical-38.test.ts → 4 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"negative","confidence":"high"},"pcom":{"state":"positive","confidence":"high"},"types":["D"],"confidence":"high"} | PASS |
| 5. A/B | clinical-38.test.ts → 5 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"indeterminate"},"types":["A_B"]} | PASS |
| 6. A/C | clinical-38.test.ts → 6 | {"od":{"state":"indeterminate"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"positive","confidence":"high"},"types":["A_C"]} | PASS |
| 7. A/D | clinical-38.test.ts → 7 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"indeterminate"},"pcom":{"state":"positive","confidence":"high"},"types":["A_D"]} | PASS |
| 8. Solo HA: no inventar B | clinical-38.test.ts → 8 | {"od":{"state":"indeterminate"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"negative","confidence":"high"},"types":["insufficient"]} | PASS |
| 9. Solo OD con HA negativa | clinical-38.test.ts → 9 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"negative","confidence":"high"},"pcom":{"state":"indeterminate"},"types":["insufficient"]} | PASS |
| 10. Solo PCOM | clinical-38.test.ts → 10 | {"od":{"state":"negative","confidence":"high"},"ha":{"state":"indeterminate"},"pcom":{"state":"positive","confidence":"high"},"types":["insufficient"]} | PASS |
| 11. A con un eje de confianza media | clinical-38.test.ts → 11 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"positive","confidence":"medium"},"types":["A"],"confidence":"moderate"} | PASS |
| 12. B con ecografía recordada normal | clinical-38.test.ts → 12 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"negative","confidence":"high"},"types":["B"]} | PASS |
| 13. C con ciclos regulares | clinical-38.test.ts → 13 | {"od":{"state":"negative","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"positive","confidence":"high"},"types":["C"]} | PASS |
| 14. D con ausencia clínica de hiperandrogenismo | clinical-38.test.ts → 14 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"negative","confidence":"high"},"pcom":{"state":"positive","confidence":"high"},"types":["D"]} | PASS |
| 15. Acné y alopecia marcados sin examen aportan HA | clinical-38.test.ts → 15 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"positive","confidence":"medium"},"pcom":{"state":"positive","confidence":"high"},"types":["A"],"confidence":"moderate"} | PASS |
| 16. DHEA-S aislada | clinical-38.test.ts → 16 | {"od":{"state":"negative","confidence":"high"},"ha":{"state":"positive","confidence":"medium"},"pcom":{"state":"positive","confidence":"high"},"types":["C"],"confidence":"moderate"} | PASS |
| 17. Anticonceptivo y andrógenos normales | clinical-38.test.ts → 17 | {"od":{"state":"positive","confidence":"high"},"pcom":{"state":"positive","confidence":"high"},"types":["probable_D","A_D"]} | PASS |
| 18. Test de LH aislado | clinical-38.test.ts → 18 | {"od":{"state":"positive","confidence":"high"},"types":["A"]} | PASS |
| 19. Amenorrea + posible FHA | clinical-38.test.ts → 19 | {"types":["conditional"],"flags":["CAUTION_FHA_PATTERN"]} | PASS |
| 20. Hiperprolactinemia activa | clinical-38.test.ts → 20 | {"types":["conditional"],"flags":["BLOCK_ACTIVE_ALT_DIAGNOSIS"]} | PASS |
| 21. Hiperandrogenismo rápidamente progresivo | clinical-38.test.ts → 21 | {"ha":{"state":"red_flag"},"types":["hard_stop"]} | PASS |
| 22. Adolescente: OD + HA | clinical-38.test.ts → 22 | {"route":"adolescent","od":{"state":"positive","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"not_used"},"types":["adolescent"]} | PASS |
| 23. Adolescente: solo OD | clinical-38.test.ts → 23 | {"route":"adolescent","od":{"state":"positive","confidence":"high"},"ha":{"state":"negative","confidence":"medium"},"pcom":{"state":"not_used"},"types":["adolescent"]} | PASS |
| 24. Perimenopausia: no convertir irregularidad nueva en OD histórica | clinical-38.test.ts → 24 | {"route":"menopause_transition","od":{"state":"negative","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"positive","confidence":"high"},"types":["historical"],"phenotype":"C"} | PASS |
| 25. Perimenopausia/postmenopausia con señal de alarma nueva | clinical-38.test.ts → 25 | {"route":"postmenopause","ha":{"state":"red_flag"},"types":["hard_stop"]} | PASS |
| 26. Inmunoensayo alto, LC-MS/MS normal | clinical-38.test.ts → 26 | {"ha":{"state":"positive"},"flags":["HA_LAB_DISCORDANCE"]} | PASS |
| 27. Hirsutismo claro con testosterona normal | clinical-38.test.ts → 27 | {"od":{"state":"positive","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"negative","confidence":"high"},"types":["B"]} | PASS |
| 28. Ciclos regulares + LH positiva solamente | clinical-38.test.ts → 28 | {"od":{"state":"negative","confidence":"high"},"types":["C"]} | PASS |
| 29. Ciclos regulares + progesterona bien temporizada | clinical-38.test.ts → 29 | {"od":{"state":"negative","confidence":"high"},"ha":{"state":"positive","confidence":"high"},"pcom":{"state":"positive","confidence":"high"},"types":["C"]} | PASS |
| 30. Progesterona baja día 21 en ciclo de 38–42 días | clinical-38.test.ts → 30 | {"od":{"state":"positive","confidence":"high"}} | PASS |
| 31. Sintotérmico repetidamente bifásico con ciclos regulares | clinical-38.test.ts → 31 | {"od":{"state":"negative","confidence":"high"},"types":["C"]} | PASS |
| 32. Ecografía transabdominal con muchos folículos, sin volumen | clinical-38.test.ts → 32 | {"pcom":{"state":"indeterminate"}} | PASS |
| 33. Ecografía transabdominal con OV 11 mL | clinical-38.test.ts → 33 | {"pcom":{"state":"positive","confidence":"high"}} | PASS |
| 34. Folículo dominante en único ovario informado | clinical-38.test.ts → 34 | {"pcom":{"state":"indeterminate"}} | PASS |
| 35. AMH alta sin ensayo/cutoff | clinical-38.test.ts → 35 | {"pcom":{"state":"indeterminate"}} | PASS |
| 36. AMH válida compatible sin ecografía | clinical-38.test.ts → 36 | {"pcom":{"state":"indeterminate"}} | PASS |
| 37. AMH baja durante ACO combinado | clinical-38.test.ts → 37 | {"pcom":{"state":"indeterminate"},"flags":["CAUTION_AMH_COCP"]} | PASS |
| 38. Ecografía adecuada negativa + AMH válida positiva | clinical-38.test.ts → 38 | {"pcom":{"state":"negative"}} | PASS |

Total: 38/38 PASS. Casos adicionales no sustituyen esta matriz.
