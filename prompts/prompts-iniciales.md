## Prompts iniciales

1. Install
```sh
openspec init
```

2. Please read openspec/project.md and help me fill it out with details about my project, tech stack, and conventions

3. I want to add: a unit test suite in Jest for the functionality of inserting candidates into database. There are 2 main families of tests, receiving the data from the form, and saving it in the database. We want to see tests that cover both processes with at least one test. Please create an OpenSpec change proposal for this feature.

## Resultado de OpenSpec

Implementación completada
Resumen de lo implementado
1. Infraestructura de tests:
Configuración de Jest en backend/jest.config.js
Utilidades de mock para Prisma (mockPrisma.ts)
Fixtures de test (testFixtures.ts)
Instalación de jest-mock-extended para mocks avanzados
2. Tests del controlador (4 tests):
Creación exitosa con datos válidos
Manejo de errores con datos inválidos
Propagación de errores de base de datos (email duplicado)
Manejo de errores desconocidos
3. Tests del servicio (5 tests):
Guardado exitoso en base de datos
Manejo de errores de validación
Violación de constraint (email duplicado P2002)
Persistencia de entidades relacionadas (educations, workExperiences, resumes)
Manejo de errores de conexión a base de datos
Resultados de los tests
Test Suites: 2 passed, 2 totalTests:       9 passed, 9 total
Cobertura de requisitos
Controller Layer Tests: 4 escenarios cubiertos
Service Layer Tests: 5 escenarios cubiertos
Al menos un test por familia: cumplido
Archivos creados
backend/jest.config.js - Configuración de Jest
backend/src/__tests__/setup.ts - Setup de tests
backend/src/__tests__/helpers/mockPrisma.ts - Utilidades de mock
backend/src/__tests__/helpers/testFixtures.ts - Fixtures de datos
backend/src/presentation/controllers/__tests__/candidateController.test.ts - Tests del controlador
backend/src/application/services/__tests__/candidateService.test.ts - Tests del servicio
Tareas completadas
Todas las tareas en tasks.md están marcadas como completadas.
La implementación cumple con los requisitos de la especificación OpenSpec y todos los tests pasan correctamente.