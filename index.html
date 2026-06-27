<script>
    const btnEnVivo = document.getElementById('btn-envivo');
    const btnProximos = document.getElementById('btn-proximos');
    const listaEnVivo = document.getElementById('contenedor-envivo');
    const listaProximos = document.getElementById('contenedor-proximos');

    // Lógica de pestañas original
    btnEnVivo.addEventListener('click', () => {
        btnEnVivo.className = 'btn-mini activo'; btnProximos.className = 'btn-mini inactivo';
        listaEnVivo.classList.remove('oculto'); listaProximos.classList.add('oculto');
    });
    btnProximos.addEventListener('click', () => {
        btnProximos.className = 'btn-mini activo'; btnEnVivo.className = 'btn-mini inactivo';
        listaProximos.classList.remove('oculto'); listaEnVivo.classList.add('oculto');
    });

    // Función que lee los datos actualizados de GitHub
    async function actualizarMarcador() {
        try {
            // Lee el archivo partidos.json que está en la misma carpeta
            const respuesta = await fetch('partidos.json?t=' + new Date().getTime()); // El ?t= evita que el navegador guarde cache viejo
            const datos = await respuesta.json();

            // Actualizar pestaña HOY
            listaEnVivo.innerHTML = '';
            datos.hoy.forEach(partido => {
                const esVivo = partido.estado.toLowerCase() === 'vivo';
                listaEnVivo.innerHTML += `
                    <div class="fila-partido ${esVivo ? 'en-vivo' : ''}">
                        <div class="equipo-caja local">
                            <span class="bandera-icono">${partido.banderaLocal}</span>
                            <span>${partido.local}</span>
                        </div>
                        <div class="score-caja">
                            <div class="num-goles ${esVivo ? 'rojo' : 'amarillo'}">${partido.goles}</div>
                            ${partido.tiempo ? `<div class="tiempo-min ${esVivo ? 'rojo' : ''}">${partido.tiempo}</div>` : ''}
                            <div class="tag-estado ${esVivo ? 'vivo' : 'fin'}">${partido.estado}</div>
                        </div>
                        <div class="equipo-caja visitante">
                            <span>${partido.visitante}</span>
                            <span class="bandera-icono">${partido.banderaVisitante}</span>
                        </div>
                    </div>
                `;
            });

            // Actualizar pestaña PRÓXIMOS
            listaProximos.innerHTML = '';
            datos.proximos.forEach(partido => {
                listaProximos.innerHTML += `
                    <div class="fila-partido">
                        <div class="equipo-caja local">
                            <span class="bandera-icono">${partido.banderaLocal}</span>
                            <span>${partido.local}</span>
                        </div>
                        <div class="score-caja">
                            <div class="num-goles gris">vs</div>
                            <div class="tiempo-min" style="color:#70a4ab;">${partido.tiempo}</div>
                            <div class="tag-estado prog">${partido.estado}</div>
                        </div>
                        <div class="equipo-caja visitante">
                            <span>${partido.visitante}</span>
                            <span class="bandera-icono">${partido.banderaVisitante}</span>
                        </div>
                    </div>
                `;
            });

        } catch (error) {
            console.error("Error al actualizar el marcador:", error);
        }
    }

    // Ejecutar al cargar la página
    actualizarMarcador();

    // Volver a revisar cambios cada 15 segundos
    setInterval(actualizarMarcador, 15000); 
</script>
