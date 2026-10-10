# SPACE1 REBORN

Reimplementación inspirada en Space1.io. Estado: **Fase 1 completada**.

    npm install
    npm run dev        # http://localhost:5173
    npm run typecheck
    npm test           # simulación + cámara
    npm run build

Al abrir el juego aparece el centro de mando. **Jugar** inicia o reinicia una partida; **Personalizar nave** permite elegir el color de la flota; **Configuración** ajusta calidad estelar y respuesta del control; **Cómo jugar** muestra los controles. Las preferencias se guardan en el dispositivo.

Cada partida comienza con una nave líder y dos escoltas. Las escoltas absorben el daño primero; si la líder pierde toda su salud, la partida termina. Mantén el botón izquierdo para que la líder y cada escolta disparen ráfagas de cuatro proyectiles rectos hacia delante; cada ráfaga tiene una pausa antes de la siguiente y soltar el botón cancela la ráfaga actual. La cadencia, cantidad y velocidad se configuran en `src/shared/constants/game.ts`. Los proyectiles alcanzan bots y asteroides en su trayectoria. Los asteroides tienen tamaño, salud, energía y colisión; destruirlos produce energía de flota. El HUD muestra **FLOTA** y **ENERGÍA**; cada 10 de energía crea una escolta adicional (coste configurable en `src/shared/constants/game.ts`). Los bots comienzan con tres naves incluyendo su líder, aparecen en ubicaciones aleatorias y pueden atacarse entre sí; también extraen asteroides para crecer.

Controles: ratón = dirigir la flota (distancia al centro = empuje); botón izquierdo mantenido = disparar ráfagas; `Esc` o **Menú** detiene la simulación y vuelve al centro de mando. El crecimiento de la flota depende de energía, no de teclas. **Salir** permite cerrar la pestaña (el navegador puede bloquear el cierre automático).
Los valores marcados [INFERIDO] en `src/shared/constants/game.ts` no proceden de ninguna fuente sobre el juego original.
