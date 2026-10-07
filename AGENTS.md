# AGENTS.md — Calculadora de Supletorio

App móvil para estudiantes de la EPN: registrar materias y las notas de sus
dos bimestres, ver el estado académico y saber qué calificación necesitan en
el supletorio. Proyecto didáctico.

## Stack y estructura
- Expo (plantilla por defecto de create-expo-app), TypeScript y Expo Router.
- Persistencia local con @react-native-async-storage/async-storage. Sin
  backend ni cuentas.
- src/domain/: lógica pura (sin React ni AsyncStorage). src/storage/:
  persistencia. app/: pantallas. Pruebas junto a cada módulo, en __tests__/.

## Comandos
- Ejecutar: npx expo start (si la red bloquea: npx expo start --tunnel)
- Pruebas: npx jest
- Tipos: npx tsc --noEmit

## Convenciones
- Código y nombres en inglés; textos de interfaz y comentarios en español.
- Las reglas de negocio de las notas están en la skill academic-rules. Las
  decisiones de cómo representarlas y validarlas se toman en la spec de cada
  historia (specs/NNN-*/decisiones.md), no se improvisan.
- Colores y contraste: skill epn-brand. Trampas de interfaz: rn-conventions.

## Forma de trabajar
- Lee docs/constitution.md y la spec activa (specs/NNN-*/) antes de tocar
  código.
- Antes de escribir código muestra el plan. Una tarea por vez.
- Si tienes dudas, pregunta antes de asumir.

## Límites
- Siempre: pruebas primero en la lógica, textos en español, actualizar
  MEMORY.md al terminar cada tarea.
- Pregunta antes: instalar dependencias, crear archivos fuera del plan,
  cambiar el formato de los datos guardados.
- Nunca: reemplazar archivos existentes sin que la tarea lo pida, ni guardar
  datos sensibles.

## Memoria
- Al empezar lee MEMORY.md; al terminar actualízalo (máximo ~50 líneas).

## Verificación
- Lógica: npx jest en verde. Interfaz: la lista manual de la tarea en Expo Go.


