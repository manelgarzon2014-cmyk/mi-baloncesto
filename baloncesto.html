<!DOCTYPE html>  
<html lang="es">  
<head>  
  <meta charset="UTF-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">  
  <title>Mi Baloncesto</title>  
  <style>  
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }  
    body { background: #f0f2f5; color: #333; padding-bottom: 80px; }  
      
    /* Cabecera */  
    header { background: #e67e22; color: white; padding: 20px; text-align: center; border-bottom-left-radius: 20px; border-bottom-right-radius: 20px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }  
    header h1 { font-size: 1.5rem; margin-bottom: 5px; }  
    header p { font-size: 0.9rem; opacity: 0.9; }  
      
    /* Formulario */  
    .container { padding: 20px; max-width: 500px; margin: 0 auto; }  
    .card { background: white; padding: 20px; border-radius: 15px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); margin-bottom: 20px; }  
      
    .form-group { margin-bottom: 15px; }  
    label { display: block; font-size: 0.9rem; font-weight: 600; margin-bottom: 5px; color: #555; }  
    input, select, textarea { width: 100%; padding: 12px; border: 1px solid #ddd; border-radius: 10px; font-size: 1rem; outline: none; }  
    input:focus, select:focus, textarea:focus { border-color: #e67e22; }  
      
    .btn-add { width: 100%; padding: 14px; background: #e67e22; color: white; border: none; border-radius: 10px; font-size: 1rem; font-weight: bold; cursor: pointer; transition: 0.2s; }  
    .btn-add:active { background: #d35400; transform: scale(0.98); }  
  
    /* Pestañas */  
    .tabs { display: flex; margin-bottom: 15px; background: #e0e0e0; border-radius: 10px; padding: 5px; }  
    .tab { flex: 1; text-align: center; padding: 10px; border-radius: 8px; font-weight: bold; color: #666; cursor: pointer; transition: 0.3s; }  
    .tab.active { background: white; color: #e67e22; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }  
  
    /* Lista de eventos */  
    .evento { background: white; padding: 15px; border-radius: 12px; margin-bottom: 10px; border-left: 5px solid #e67e22; box-shadow: 0 2px 8px rgba(0,0,0,0.05); display: flex; justify-content: space-between; align-items: center; }  
    .evento-info h3 { font-size: 1.1rem; color: #333; margin-bottom: 3px; }  
    .evento-info p { font-size: 0.85rem; color: #777; }  
    .evento-info .notas { font-size: 0.85rem; color: #555; margin-top: 5px; font-style: italic; }  
    .btn-delete { background: transparent; border: none; color: #e74c3c; font-size: 1.5rem; cursor: pointer; padding: 5px; }  
      
    .empty-state { text-align: center; color: #999; padding: 20px; font-size: 1rem; }  
  </style>  
</head>  
<body>  
  
  <header>  
    <h1>🏀 Mi Baloncesto</h1>  
    <p id="stats">0 Entrenamientos | 0 Partidos</p>  
  </header>  
  
  <div class="container">  
      
    <!-- Formulario -->  
    <div class="card">  
      <div class="form-group">  
        <label>Tipo de sesión</label>  
        <select id="tipo">  
          <option value="Entrenamiento">🏃 Entrenamiento</option>  
          <option value="Partido">🏆 Partido</option>  
        </select>  
      </div>  
      <div class="form-group">  
        <label>Fecha</label>  
        <input type="date" id="fecha">  
      </div>  
      <div class="form-group">  
        <label>Duración (minutos)</label>  
        <input type="number" id="duracion" placeholder="Ej: 90" min="1">  
      </div>  
      <div class="form-group">  
        <label id="label-extra">Título / Rival</label>  
        <input type="text" id="titulo" placeholder="Ej: Ejercicios de tiro / Equipo rival">  
      </div>  
      <div class="form-group">  
        <label>Notas (opcional)</label>  
        <textarea id="notas" rows="2" placeholder="Cómo fue la sesión..."></textarea>  
      </div>  
      <button class="btn-add" onclick="añadirEvento()">Guardar</button>  
    </div>  
  
    <!-- Pestañas para filtrar -->  
    <div class="tabs">  
      <div class="tab active" onclick="filtrar('Todos', this)">Todos</div>  
      <div class="tab" onclick="filtrar('Entrenamiento', this)">Entrenos</div>  
      <div class="tab" onclick="filtrar('Partido', this)">Partidos</div>  
    </div>  
  
    <!-- Lista -->  
    <div id="lista"></div>  
  </div>  
  
  <script>  
    // Cargar datos guardados o iniciar vacío  
    let eventos = JSON.parse(localStorage.getItem('baloncesto') || '[]');  
    let filtroActual = 'Todos';  
  
    // Poner fecha de hoy por defecto  
    document.getElementById('fecha').valueAsDate = new Date();  
  
    function guardarDatos() {  
      localStorage.setItem('baloncesto', JSON.stringify(eventos));  
    }  
  
    function actualizarStats() {  
      const entrenos = eventos.filter(e => e.tipo === 'Entrenamiento').length;  
      const partidos = eventos.filter(e => e.tipo === 'Partido').length;  
      document.getElementById('stats').innerText = `${entrenos} Entrenamientos | ${partidos} Partidos`;  
    }  
  
    function añadirEvento() {  
      const tipo = document.getElementById('tipo').value;  
      const fecha = document.getElementById('fecha').value;  
      const duracion = document.getElementById('duracion').value;  
      const titulo = document.getElementById('titulo').value;  
      const notas = document.getElementById('notas').value;  
  
      if (!fecha || !titulo) {  
        alert('Por favor, rellena la fecha y el título/rival.');  
        return;  
      }  
  
      const nuevoEvento = {  
        id: Date.now(),  
        tipo: tipo,  
        fecha: fecha,  
        duracion: duracion || '0',  
        titulo: titulo,  
        notas: notas  
      };  
  
      eventos.unshift(nuevoEvento); // Añadir al principio  
      guardarDatos();  
      renderizar();  
        
      // Limpiar formulario  
      document.getElementById('duracion').value = '';  
      document.getElementById('titulo').value = '';  
      document.getElementById('notas').value = '';  
    }  
  
    function eliminarEvento(id) {  
      if(confirm('¿Seguro que quieres borrar este registro?')) {  
        eventos = eventos.filter(e => e.id !== id);  
        guardarDatos();  
        renderizar();  
      }  
    }  
  
    function filtrar(filtro, boton) {  
      filtroActual = filtro;  
      // Cambiar estilo de pestañas  
      document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));  
      boton.classList.add('active');  
      renderizar();  
    }  
  
    function renderizar() {  
      actualizarStats();  
      const lista = document.getElementById('lista');  
      lista.innerHTML = '';  
  
      let eventosFiltrados = eventos;  
      if (filtroActual !== 'Todos') {  
        eventosFiltrados = eventos.filter(e => e.tipo === filtroActual);  
      }  
  
      if (eventosFiltrados.length === 0) {  
        lista.innerHTML = '<p class="empty-state">No hay registros aquí todavía. ¡A entrenar! 🏀</p>';  
        return;  
      }  
  
      eventosFiltrados.forEach(evento => {  
        const div = document.createElement('div');  
        div.className = 'evento';  
          
        // Formatear fecha (de AAAA-MM-DD a DD/MM/AAAA)  
        const fechaParts = evento.fecha.split('-');  
        const fechaFormateada = fechaParts.length === 3 ? `${fechaParts[2]}/${fechaParts[1]}/${fechaParts[0]}` : evento.fecha;  
  
        div.innerHTML = `  
          <div class="evento-info">  
            <h3>${evento.tipo === 'Partido' ? '🏆' : '🏃'} ${evento.titulo}</h3>  
            <p>📅 ${fechaFormateada} | ⏱️ ${evento.duracion} min</p>  
            ${evento.notas ? `<p class="notas">"${evento.notas}"</p>` : ''}  
          </div>  
          <button class="btn-delete" onclick="eliminarEvento(${evento.id})">✕</button>  
        `;  
        lista.appendChild(div);  
      });  
    }  
  
    // Cambiar texto del input según el tipo seleccionado  
    document.getElementById('tipo').addEventListener('change', function() {  
      const label = document.getElementById('label-extra');  
      const input = document.getElementById('titulo');  
      if (this.value === 'Partido') {  
        label.innerText = 'Nombre del Rival / Torneo';  
        input.placeholder = 'Ej: Contra los Lakers';  
      } else {  
        label.innerText = 'Título del entrenamiento';  
        input.placeholder = 'Ej: Tiros libres y defensa';  
      }  
    });  
  
    // Iniciar app  
    renderizar();  
  </script>  
</body>  
</html>  
