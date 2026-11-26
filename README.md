# Mi Tarjeta de Horas

App web para el celular que lleva el control de asistencia de un trabajador en Bolivia (Santa Cruz de la Sierra).

## Qué hace

- **Marcación**: botón de entrada y, desde las 15:00, botón de salida.
- **Horas extra**: si entras antes de tu hora de ingreso, esos minutos cuentan como extra. Por la tarde, solo hay extra si sales después de las 18:50, y se cuenta desde las 19:00. En día de descanso, todo lo trabajado cuenta como extra. Cada hora extra se paga al doble: `haber básico ÷ 30 ÷ 8 × 2`.
- **Feriados**: el calendario de Bolivia (DS 2750 y DS 5521 para 2026) y el de Santa Cruz (24 de septiembre) se calculan solos. Si un feriado cae domingo, pasa al lunes, salvo Carnaval, Viernes Santo, Corpus Christi y el 2 de noviembre. Un feriado trabajado en día de descanso suma 2 días de compensación; en día laboral, 1 día. También puedes agregar feriados por decreto o marcar uno como no aplicado.
- **Vacaciones** (Ley General del Trabajo, Art. 44): se calculan desde tu fecha de ingreso. Corresponden 15 días hábiles de 1 a 5 años, 20 de 5 a 10 años y 30 desde los 10 años. Anotas los días tomados en cada gestión cumplida.
- **Saldos**: descuentan las devoluciones de días de feriado, las horas extra devueltas en tiempo libre y las horas extra pagadas.

## Uso

Abre `index.html` en el navegador. Fuera de claude.ai, los datos se guardan en el `localStorage` de ese navegador. En la versión publicada en claude.ai, se guardan en la base de datos del artifact, y solo el dueño puede leerla y modificarla.

El cambio de feriados para un año nuevo se hace en el objeto `DECRETOS` dentro de `index.html`.
