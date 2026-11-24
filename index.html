<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bitácora de Mantenimiento de Equipos</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fafc;
        }
        /* Animaciones suaves para modales y tarjetas */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .animate-fade-in {
            animation: fadeIn 0.3s ease-out forwards;
        }
    </style>
</head>
<body class="text-slate-800 antialiased min-h-screen flex flex-col">

    <!-- Barra de Navegación Superior -->
    <header class="bg-slate-900 text-white shadow-md sticky top-0 z-30">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <div class="flex items-center space-x-3">
                <div class="bg-amber-500 p-2 rounded-xl text-slate-900 shadow-sm">
                    <i data-lucide="wrench" class="w-6 h-6"></i>
                </div>
                <div>
                    <div class="flex items-center gap-2">
                        <h1 class="text-lg sm:text-xl font-bold tracking-tight leading-none">ManteniApp</h1>
                        <span id="admin-badge" class="hidden px-2 py-0.5 text-[10px] font-bold uppercase tracking-wider bg-amber-500 text-slate-900 rounded-md">
                            Admin
                        </span>
                    </div>
                    <p class="text-xs text-slate-400 hidden sm:block">Control Diario y Evidencia Fotográfica</p>
                </div>
            </div>

            <!-- Controles de Usuario y Modo Administrador -->
            <div class="flex items-center space-x-2 sm:space-x-3">
                <button id="btn-admin-toggle" class="flex items-center space-x-1.5 bg-slate-800 hover:bg-slate-700 border border-slate-700 px-2.5 py-1.5 rounded-xl text-xs sm:text-sm transition cursor-pointer" title="Acceso Administrador">
                    <i data-lucide="shield" id="admin-icon" class="w-4 h-4 text-slate-400"></i>
                    <span id="admin-btn-text" class="hidden sm:inline font-medium text-slate-300">Admin</span>
                </button>

                <button id="btn-change-user" class="flex items-center space-x-2 bg-slate-800 hover:bg-slate-700 border border-slate-700 px-3 py-1.5 rounded-xl text-sm transition cursor-pointer" title="Cambiar nombre de técnico">
                    <div class="w-6 h-6 rounded-full bg-amber-500/20 text-amber-400 flex items-center justify-center font-bold text-xs" id="user-avatar">
                        ?
                    </div>
                    <span id="current-user-display" class="font-medium max-w-[100px] sm:max-w-[160px] truncate">Cargando...</span>
                    <i data-lucide="edit-2" class="w-3.5 h-3.5 text-slate-400"></i>
                </button>
            </div>
        </div>
    </header>

    <!-- Pantalla de Acceso Restringido (Oculta los reportes hasta validar acceso) -->
    <div id="access-gate" class="flex-grow flex items-center justify-center px-4 py-10">
        <div class="bg-white max-w-md w-full rounded-2xl shadow-md border border-slate-200/90 p-6 sm:p-7 animate-fade-in">
            <div class="w-12 h-12 rounded-2xl bg-slate-900 text-amber-400 flex items-center justify-center mb-4">
                <i data-lucide="lock" class="w-6 h-6"></i>
            </div>
            <h2 class="text-xl font-bold text-slate-900">Bitácora Privada de Mantenimiento</h2>
            <p class="text-sm text-slate-500 mt-1 mb-5">
                Los reportes cargados son privados. Ingresa el código de acceso del equipo para cargar reportes o tu clave de administrador para gestionar y borrar registros.
            </p>

            <form id="access-gate-form" class="space-y-4">
                <div>
                    <label for="gate-access-code" class="block text-sm font-medium text-slate-700 mb-1">Código de Acceso</label>
                    <input type="password" id="gate-access-code" required placeholder="Ingresa código de equipo o PIN admin"
                        class="w-full px-4 py-2.5 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 outline-none transition">
                    <p id="gate-error-msg" class="hidden text-xs text-red-600 font-medium mt-1.5">Código incorrecto. Verifica con tu supervisor.</p>
                </div>

                <button type="submit" class="w-full bg-amber-500 hover:bg-amber-600 text-slate-900 font-semibold py-2.5 px-4 rounded-xl transition flex items-center justify-center gap-2 cursor-pointer">
                    <i data-lucide="unlock" class="w-4 h-4"></i>
                    <span>Ingresar a la Bitácora</span>
                </button>
            </form>
        </div>
    </div>

    <!-- Contenedor Principal (Oculto hasta ingresar con código válido) -->
    <main id="main-app-content" class="hidden flex-grow max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-6 sm:py-8">
        
        <!-- Tarjetas de Resumen / Estadísticas Rápidas -->
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-3 sm:gap-4 mb-6">
            <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200/80 flex items-center space-x-3">
                <div class="p-3 rounded-xl bg-blue-50 text-blue-600">
                    <i data-lucide="clipboard-list" class="w-6 h-6"></i>
                </div>
                <div>
                    <p class="text-xs font-medium text-slate-500">Total Reportes</p>
                    <p id="stat-total" class="text-xl sm:text-2xl font-bold text-slate-800">0</p>
                </div>
            </div>
            <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200/80 flex items-center space-x-3">
                <div class="p-3 rounded-xl bg-emerald-50 text-emerald-600">
                    <i data-lucide="calendar-check" class="w-6 h-6"></i>
                </div>
                <div>
                    <p class="text-xs font-medium text-slate-500">Hoy</p>
                    <p id="stat-today" class="text-xl sm:text-2xl font-bold text-slate-800">0</p>
                </div>
            </div>
            <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200/80 flex items-center space-x-3">
                <div class="p-3 rounded-xl bg-amber-50 text-amber-600">
                    <i data-lucide="alert-triangle" class="w-6 h-6"></i>
                </div>
                <div>
                    <p class="text-xs font-medium text-slate-500">En Revisión</p>
                    <p id="stat-warning" class="text-xl sm:text-2xl font-bold text-slate-800">0</p>
                </div>
            </div>
            <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200/80 flex items-center space-x-3">
                <div class="p-3 rounded-xl bg-purple-50 text-purple-600">
                    <i data-lucide="users" class="w-6 h-6"></i>
                </div>
                <div>
                    <p class="text-xs font-medium text-slate-500">Técnicos Activos</p>
                    <p id="stat-users" class="text-xl sm:text-2xl font-bold text-slate-800">0</p>
                </div>
            </div>
        </div>

        <!-- Layout de 2 Columnas: Formulario (Izquierda) y Bitácora (Derecha) -->
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 sm:gap-8 items-start">
            
            <!-- Columna Izquierda: Formulario de Nuevo Reporte -->
            <section class="lg:col-span-5 bg-white rounded-2xl shadow-sm border border-slate-200/80 p-5 sm:p-6">
                <div class="flex items-center justify-between mb-5">
                    <h2 class="text-lg font-bold text-slate-800 flex items-center gap-2">
                        <i data-lucide="plus-circle" class="w-5 h-5 text-amber-500"></i>
                        Nuevo Registro Diario
                    </h2>
                    <span class="text-xs font-medium px-2.5 py-1 bg-slate-100 text-slate-600 rounded-lg" id="today-date-badge">
                        Hoy
                    </span>
                </div>

                <form id="maintenance-form" class="space-y-4">
                    <!-- Equipo / Maquinaria -->
                    <div>
                        <label for="equipment-name" class="block text-sm font-medium text-slate-700 mb-1">Equipo o Maquinaria *</label>
                        <div class="relative">
                            <input type="text" id="equipment-name" required placeholder="Ej. Compresor #2, Torno CNC, Generador..." 
                                class="w-full pl-10 pr-4 py-2.5 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 focus:border-amber-500 outline-none transition">
                            <i data-lucide="cpu" class="w-4 h-4 text-slate-400 absolute left-3.5 top-3"></i>
                        </div>
                    </div>

                    <!-- Tipo de Mantenimiento y Estado -->
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                        <div>
                            <label for="maintenance-type" class="block text-sm font-medium text-slate-700 mb-1">Tipo</label>
                            <select id="maintenance-type" class="w-full px-3 py-2.5 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 focus:border-amber-500 outline-none transition">
                                <option value="Preventivo">Preventivo</option>
                                <option value="Correctivo">Correctivo</option>
                                <option value="Inspección">Inspección Diaria</option>
                                <option value="Limpieza">Limpieza / Lubricación</option>
                            </select>
                        </div>
                        <div>
                            <label for="equipment-status" class="block text-sm font-medium text-slate-700 mb-1">Estado Final</label>
                            <select id="equipment-status" class="w-full px-3 py-2.5 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 focus:border-amber-500 outline-none transition">
                                <option value="Operativo">🟢 Operativo</option>
                                <option value="Observación">🟡 En Observación</option>
                                <option value="Fuera de Servicio">🔴 Fuera de Servicio</option>
                            </select>
                        </div>
                    </div>

                    <!-- Subida de Fotografía -->
                    <div>
                        <label class="block text-sm font-medium text-slate-700 mb-1">Evidencia Fotográfica *</label>
                        <div id="drop-zone" class="border-2 border-dashed border-slate-300 hover:border-amber-500 bg-slate-50 rounded-2xl p-4 text-center cursor-pointer transition relative overflow-hidden">
                            <input type="file" id="photo-input" accept="image/*" capture="environment" class="hidden">
                            
                            <!-- Estado sin imagen -->
                            <div id="upload-placeholder" class="py-4 flex flex-col items-center justify-center">
                                <div class="w-12 h-12 rounded-full bg-amber-100 text-amber-600 flex items-center justify-center mb-2">
                                    <i data-lucide="camera" class="w-6 h-6"></i>
                                </div>
                                <p class="text-sm font-medium text-slate-700">Toca para tomar foto o subir imagen</p>
                                <p class="text-xs text-slate-400 mt-1">JPG, PNG o WEBP (Optimización automática)</p>
                            </div>

                            <!-- Vista previa de imagen -->
                            <div id="image-preview-container" class="hidden relative">
                                <img id="image-preview" src="" alt="Vista previa" class="w-full h-48 object-cover rounded-xl shadow-sm">
                                <button type="button" id="btn-remove-photo" class="absolute top-2 right-2 bg-slate-900/80 hover:bg-red-600 text-white p-1.5 rounded-lg backdrop-blur-sm transition" title="Quitar foto">
                                    <i data-lucide="trash-2" class="w-4 h-4"></i>
                                </button>
                            </div>
                        </div>
                    </div>

                    <!-- Descripción del trabajo realizado -->
                    <div>
                        <label for="description" class="block text-sm font-medium text-slate-700 mb-1">Descripción de actividades *</label>
                        <textarea id="description" rows="3" required placeholder="Detalla las tareas realizadas, piezas cambiadas, lecturas o anomalías encontradas..." 
                            class="w-full p-3 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 focus:border-amber-500 outline-none transition resize-none"></textarea>
                    </div>

                    <!-- Botón Enviar -->
                    <button type="submit" id="btn-submit" class="w-full bg-amber-500 hover:bg-amber-600 active:bg-amber-700 text-slate-900 font-semibold py-3 px-4 rounded-xl shadow-sm transition flex items-center justify-center gap-2 cursor-pointer">
                        <i data-lucide="send" class="w-4 h-4"></i>
                        <span>Guardar Reporte en Bitácora</span>
                    </button>

                    <!-- Aviso cuando el Modo Administrador está activo -->
                    <div id="admin-form-lock-notice" class="hidden bg-amber-50 border border-amber-200 text-amber-800 rounded-xl p-3 text-xs flex items-center justify-between gap-2">
                        <div class="flex items-center gap-2">
                            <i data-lucide="shield-alert" class="w-4 h-4 text-amber-600 flex-shrink-0"></i>
                            <span>Modo Admin activo: carga bloqueada para evitar reportes accidentales.</span>
                        </div>
                        <button type="button" id="btn-exit-admin-from-form" class="font-semibold underline hover:text-amber-950 whitespace-nowrap cursor-pointer">
                            Salir Admin
                        </button>
                    </div>
                </form>
            </section>

            <!-- Columna Derecha: Historial y Filtros -->
            <section class="lg:col-span-7 space-y-4">
                
                <!-- Barra de Filtros -->
                <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200/80 flex flex-col sm:flex-row gap-3">
                    <div class="relative flex-grow">
                        <input type="text" id="filter-search" placeholder="Buscar por equipo, técnico o detalle..." 
                            class="w-full pl-9 pr-4 py-2 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 outline-none">
                        <i data-lucide="search" class="w-4 h-4 text-slate-400 absolute left-3 top-2.5"></i>
                    </div>
                    <div class="flex gap-2">
                        <select id="filter-status" class="px-3 py-2 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 outline-none">
                            <option value="ALL">Todos los estados</option>
                            <option value="Operativo">Operativo</option>
                            <option value="Observación">En Observación</option>
                            <option value="Fuera de Servicio">Fuera de Servicio</option>
                        </select>
                        <input type="date" id="filter-date" class="px-3 py-2 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 outline-none" title="Filtrar por fecha">
                    </div>
                </div>

                <!-- Lista de Reportes -->
                <div id="reports-container" class="space-y-4">
                    <!-- Estado de carga inicial -->
                    <div id="loading-state" class="bg-white rounded-2xl p-12 text-center border border-slate-200/80">
                        <div class="inline-block animate-spin rounded-full h-8 w-8 border-4 border-amber-500 border-t-transparent mb-3"></div>
                        <p class="text-slate-500 text-sm font-medium">Sincronizando bitácora del equipo...</p>
                    </div>
                </div>

            </section>
        </div>
    </main>

    <!-- Modal para Identificación del Usuario -->
    <div id="user-modal" class="fixed inset-0 bg-slate-900/70 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-md w-full p-6 shadow-xl animate-fade-in">
            <div class="w-12 h-12 rounded-2xl bg-amber-100 text-amber-600 flex items-center justify-center mb-4">
                <i data-lucide="user-check" class="w-6 h-6"></i>
            </div>
            <h3 class="text-xl font-bold text-slate-900 mb-1">Identificación de Técnico</h3>
            <p class="text-sm text-slate-500 mb-4">Ingresa tu nombre y apellido para que tus reportes queden firmados en la bitácora compartida.</p>
            
            <form id="user-form" class="space-y-4">
                <div>
                    <label for="input-username" class="block text-sm font-medium text-slate-700 mb-1">Nombre completo</label>
                    <input type="text" id="input-username" required placeholder="Ej. Carlos Mendoza" 
                        class="w-full px-4 py-2.5 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 outline-none">
                </div>
                <div class="bg-slate-50 p-3 rounded-xl border border-slate-200/80">
                    <p class="text-xs text-slate-500">ID de sesión asignado:</p>
                    <p id="modal-user-id" class="text-xs font-mono text-slate-700 break-all mt-0.5">Autenticando...</p>
                </div>
                <button type="submit" class="w-full bg-slate-900 hover:bg-slate-800 text-white font-semibold py-2.5 px-4 rounded-xl transition cursor-pointer">
                    Confirmar y Continuar
                </button>
            </form>
        </div>
    </div>

    <!-- Modal para Ingresar PIN de Administrador -->
    <div id="admin-modal" class="fixed inset-0 bg-slate-900/70 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-sm w-full p-6 shadow-xl animate-fade-in">
            <div class="w-12 h-12 rounded-2xl bg-slate-900 text-amber-400 flex items-center justify-center mb-4">
                <i data-lucide="shield-check" class="w-6 h-6"></i>
            </div>
            <h3 class="text-lg font-bold text-slate-900 mb-1">Acceso Administrador</h3>
            <p class="text-sm text-slate-500 mb-4">Ingresa tu clave de administrador para eliminar reportes cargados por error.</p>
            
            <form id="admin-form" class="space-y-4">
                <div>
                    <label for="input-admin-pin" class="block text-sm font-medium text-slate-700 mb-1">Clave / PIN</label>
                    <input type="password" id="input-admin-pin" required placeholder="••••" 
                        class="w-full px-4 py-2.5 bg-slate-50 border border-slate-300 rounded-xl text-sm text-center tracking-widest font-bold focus:ring-2 focus:ring-amber-500 outline-none">
                </div>
                <div class="flex gap-3">
                    <button type="button" id="cancel-admin" class="flex-1 py-2.5 px-4 bg-slate-100 hover:bg-slate-200 text-slate-700 font-medium rounded-xl transition cursor-pointer">
                        Cancelar
                    </button>
                    <button type="submit" class="flex-1 py-2.5 px-4 bg-slate-900 hover:bg-slate-800 text-white font-semibold rounded-xl transition cursor-pointer">
                        Activar
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- Modal para Editar / Corregir Reporte -->
    <div id="edit-modal" class="fixed inset-0 bg-slate-900/70 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-md w-full p-6 shadow-xl animate-fade-in max-h-[90vh] overflow-y-auto">
            <div class="flex items-center justify-between mb-4">
                <div class="flex items-center gap-2.5">
                    <div class="w-10 h-10 rounded-xl bg-amber-100 text-amber-600 flex items-center justify-center">
                        <i data-lucide="edit-3" class="w-5 h-5"></i>
                    </div>
                    <div>
                        <h3 class="text-lg font-bold text-slate-900 leading-tight">Corregir Reporte</h3>
                        <p class="text-xs text-slate-500" id="edit-report-author">Técnico</p>
                    </div>
                </div>
                <button type="button" id="close-edit-modal" class="text-slate-400 hover:text-slate-600 p-1 rounded-lg">
                    <i data-lucide="x" class="w-5 h-5"></i>
                </button>
            </div>
            
            <form id="edit-form" class="space-y-4">
                <input type="hidden" id="edit-report-id">
                <div>
                    <label for="edit-equipment" class="block text-sm font-medium text-slate-700 mb-1">Equipo o Maquinaria</label>
                    <input type="text" id="edit-equipment" required 
                        class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 outline-none">
                </div>

                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label for="edit-type" class="block text-sm font-medium text-slate-700 mb-1">Tipo</label>
                        <select id="edit-type" class="w-full px-3 py-2.5 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 outline-none">
                            <option value="Preventivo">Preventivo</option>
                            <option value="Correctivo">Correctivo</option>
                            <option value="Inspección">Inspección Diaria</option>
                            <option value="Limpieza">Limpieza / Lubricación</option>
                        </select>
                    </div>
                    <div>
                        <label for="edit-status" class="block text-sm font-medium text-slate-700 mb-1">Estado Final</label>
                        <select id="edit-status" class="w-full px-3 py-2.5 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 outline-none">
                            <option value="Operativo">🟢 Operativo</option>
                            <option value="Observación">🟡 En Observación</option>
                            <option value="Fuera de Servicio">🔴 Fuera de Servicio</option>
                        </select>
                    </div>
                </div>

                <div>
                    <label for="edit-description" class="block text-sm font-medium text-slate-700 mb-1">Descripción corregida</label>
                    <textarea id="edit-description" rows="4" required 
                        class="w-full p-3 bg-slate-50 border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-amber-500 outline-none resize-none"></textarea>
                </div>

                <div class="flex gap-3 pt-2">
                    <button type="button" id="cancel-edit" class="flex-1 py-2.5 px-4 bg-slate-100 hover:bg-slate-200 text-slate-700 font-medium rounded-xl transition cursor-pointer">
                        Cancelar
                    </button>
                    <button type="submit" id="save-edit-btn" class="flex-1 py-2.5 px-4 bg-amber-500 hover:bg-amber-600 text-slate-900 font-semibold rounded-xl transition cursor-pointer">
                        Guardar Cambios
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- Modal para Ver Imagen en Grande -->
    <div id="lightbox-modal" class="fixed inset-0 bg-slate-950/90 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <button id="close-lightbox" class="absolute top-4 right-4 bg-white/10 hover:bg-white/20 text-white p-2.5 rounded-full transition cursor-pointer">
            <i data-lucide="x" class="w-6 h-6"></i>
        </button>
        <div class="max-w-4xl max-h-[90vh] flex flex-col items-center">
            <img id="lightbox-img" src="" alt="Evidencia ampliada" class="max-h-[75vh] w-auto rounded-2xl shadow-2xl object-contain">
            <div class="mt-4 text-center text-white max-w-2xl">
                <h4 id="lightbox-title" class="font-bold text-lg"></h4>
                <p id="lightbox-desc" class="text-sm text-slate-300 mt-1"></p>
            </div>
        </div>
    </div>

    <!-- Modal de Confirmación para Eliminar -->
    <div id="delete-modal" class="fixed inset-0 bg-slate-900/70 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-sm w-full p-6 shadow-xl animate-fade-in">
            <div class="w-12 h-12 rounded-2xl bg-red-100 text-red-600 flex items-center justify-center mb-4">
                <i data-lucide="alert-circle" class="w-6 h-6"></i>
            </div>
            <h3 class="text-lg font-bold text-slate-900 mb-1">¿Eliminar este reporte?</h3>
            <p class="text-sm text-slate-500 mb-5">Esta acción borrará permanentemente el registro y su fotografía para todos los usuarios.</p>
            <div class="flex gap-3">
                <button id="cancel-delete" class="flex-1 py-2.5 px-4 bg-slate-100 hover:bg-slate-200 text-slate-700 font-medium rounded-xl transition cursor-pointer">
                    Cancelar
                </button>
                <button id="confirm-delete" class="flex-1 py-2.5 px-4 bg-red-600 hover:bg-red-700 text-white font-medium rounded-xl transition cursor-pointer">
                    Eliminar
                </button>
            </div>
        </div>
    </div>

    <!-- Notificación Toast (Reemplazo elegante de alert) -->
    <div id="toast" class="fixed bottom-5 right-5 z-50 transform translate-y-20 opacity-0 transition-all duration-300 pointer-events-none">
        <div class="bg-slate-900 text-white px-4 py-3 rounded-xl shadow-lg flex items-center space-x-3 border border-slate-700">
            <span id="toast-icon-wrapper" class="flex items-center justify-center">
                <i data-lucide="check-circle" class="w-5 h-5 text-emerald-400"></i>
            </span>
            <span id="toast-message" class="text-sm font-medium">Operación exitosa</span>
        </div>
    </div>

    <!-- Lógica de la Aplicación con Firebase Firestore -->
    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getAuth, signInAnonymously, signInWithCustomToken, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
        import { getFirestore, collection, addDoc, updateDoc, deleteDoc, doc, onSnapshot, setDoc, getDoc } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

        // Inicializar iconos Lucide
        lucide.createIcons();

        // =========================================================================
        // CONFIGURACIÓN DE ACCESO, ADMINISTRADOR Y CONEXIÓN FIREBASE
        // =========================================================================
        const CLAVE_ADMINISTRADOR = "1234"; // <-- Cambia este PIN por la clave secreta que tú elijas
        const CODIGO_EQUIPO = "MANT2026";     // <-- Cambia este código por el que compartirás a tus técnicos

        const miConfiguracionFirebase = {
            apiKey: "AIzaSyCL2WqqY7tOtDi7OdtDFVEGilRhgATg9OM",
            authDomain: "mantenimiento-de-campo.firebaseapp.com",
            projectId: "mantenimiento-de-campo",
            storageBucket: "mantenimiento-de-campo.firebasestorage.app",
            messagingSenderId: "20533056973",
            appId: "1:20533056973:web:c3e61079c6b624e8e6e084",
            measurementId: "G-6N4ZMKMZXF"
        };

        // Detectar automáticamente si estamos en la vista previa o en tu sitio web publicado
        const appId = typeof __app_id !== 'undefined' ? __app_id : 'mantenimiento-de-campo';
        const firebaseConfig = typeof __firebase_config !== 'undefined' 
            ? JSON.parse(__firebase_config) 
            : miConfiguracionFirebase;

        // Inicializar Firebase
        const app = initializeApp(firebaseConfig);
        const auth = getAuth(app);
        const db = getFirestore(app);

        // Estado global de la aplicación
        let currentUser = null;
        let technicianName = '';
        let hasTeamAccess = localStorage.getItem('manteniapp_has_access') === 'true';
        let isAdmin = localStorage.getItem('manteniapp_is_admin') === 'true';
        let compressedImageDataUrl = null;
        let allReports = [];
        let reportToDeleteId = null;
        let unsubscribeReports = null;

        // Referencias DOM de Acceso Restringido
        const accessGate = document.getElementById('access-gate');
        const mainAppContent = document.getElementById('main-app-content');
        const accessGateForm = document.getElementById('access-gate-form');
        const gateAccessCode = document.getElementById('gate-access-code');
        const gateErrorMsg = document.getElementById('gate-error-msg');

        // Referencias DOM Admin y Edición
        const btnAdminToggle = document.getElementById('btn-admin-toggle');
        const adminBadge = document.getElementById('admin-badge');
        const adminBtnText = document.getElementById('admin-btn-text');
        const adminModal = document.getElementById('admin-modal');
        const adminForm = document.getElementById('admin-form');
        const inputAdminPin = document.getElementById('input-admin-pin');
        const cancelAdmin = document.getElementById('cancel-admin');

        const dropZone = document.getElementById('drop-zone');
        // Actualizar interfaz según estado de Acceso y Administrador
        function updateAdminUI() {
            const isAuthorized = hasTeamAccess || isAdmin;

            if (!isAuthorized) {
                accessGate.classList.remove('hidden');
                mainAppContent.classList.add('hidden');
                adminBadge.classList.add('hidden');
                btnAdminToggle.classList.remove('border-amber-500/60', 'bg-amber-500/10');
                adminBtnText.textContent = 'Admin';
                adminBtnText.classList.replace('text-amber-400', 'text-slate-300');
                allReports = [];
                if (typeof unsubscribeReports === 'function') {
                    unsubscribeReports();
                    unsubscribeReports = null;
                }
                lucide.createIcons();
                return;
            }

            accessGate.classList.add('hidden');
            mainAppContent.classList.remove('hidden');

            const formControls = maintenanceForm.querySelectorAll('input, select, textarea');

            if (isAdmin) {
                adminBadge.classList.remove('hidden');
                btnAdminToggle.classList.add('border-amber-500/60', 'bg-amber-500/10');
                adminBtnText.textContent = 'Salir Admin';
                adminBtnText.classList.replace('text-slate-300', 'text-amber-400');

                // Bloquear formulario de carga para evitar registros accidentales en modo supervisión
                formControls.forEach(el => {
                    el.disabled = true;
                    el.classList.add('opacity-60', 'cursor-not-allowed');
                });
                dropZone.classList.add('opacity-60', 'pointer-events-none');
                btnSubmit.disabled = true;
                btnSubmit.classList.add('opacity-50', 'cursor-not-allowed');
                adminFormLockNotice.classList.remove('hidden');
            } else {
                adminBadge.classList.add('hidden');
                btnAdminToggle.classList.remove('border-amber-500/60', 'bg-amber-500/10');
                adminBtnText.textContent = 'Admin';
                adminBtnText.classList.replace('text-amber-400', 'text-slate-300');

                // Habilitar formulario de carga para que los técnicos solo carguen reportes
                formControls.forEach(el => {
                    el.disabled = false;
                    el.classList.remove('opacity-60', 'cursor-not-allowed');
                });
                dropZone.classList.remove('opacity-60', 'pointer-events-none');
                btnSubmit.disabled = false;
                btnSubmit.classList.remove('opacity-50', 'cursor-not-allowed');
                adminFormLockNotice.classList.add('hidden');
            }
            lucide.createIcons();
            renderReports();
        }

        // Validar código de ingreso para evitar que cualquiera vea los reportes
        accessGateForm.addEventListener('submit', (e) => {
            e.preventDefault();
            const code = gateAccessCode.value.trim();
            gateErrorMsg.classList.add('hidden');

            if (code === CLAVE_ADMINISTRADOR) {
                isAdmin = true;
                hasTeamAccess = true;
                localStorage.setItem('manteniapp_is_admin', 'true');
                localStorage.setItem('manteniapp_has_access', 'true');
                gateAccessCode.value = '';
                updateAdminUI();
                if (currentUser) {
                    loadTechnicianProfile(currentUser.uid);
                    subscribeToReports();
                }
                showToast("Acceso Administrador concedido");
            } else if (code === CODIGO_EQUIPO) {
                hasTeamAccess = true;
                localStorage.setItem('manteniapp_has_access', 'true');
                gateAccessCode.value = '';
                updateAdminUI();
                if (currentUser) {
                    loadTechnicianProfile(currentUser.uid);
                    subscribeToReports();
                }
                showToast("Acceso concedido a la bitácora");
            } else {
                gateErrorMsg.classList.remove('hidden');
                gateAccessCode.value = '';
                gateAccessCode.focus();
            }
        });

        function disableAdminMode() {
            isAdmin = false;
            localStorage.removeItem('manteniapp_is_admin');
            updateAdminUI();
            showToast("Modo Administrador desactivado");
        }

        btnAdminToggle.addEventListener('click', () => {
            if (isAdmin) {
                disableAdminMode();
            } else {
                inputAdminPin.value = '';
                adminModal.classList.remove('hidden');
                setTimeout(() => inputAdminPin.focus(), 100);
            }
        });

        btnExitAdminFromForm.addEventListener('click', () => {
            disableAdminMode();
        });

        cancelAdmin.addEventListener('click', () => {
            adminModal.classList.add('hidden');
        });

        adminForm.addEventListener('submit', (e) => {
            e.preventDefault();
            if (inputAdminPin.value === CLAVE_ADMINISTRADOR) {
                isAdmin = true;
                localStorage.setItem('manteniapp_is_admin', 'true');
                adminModal.classList.add('hidden');
                updateAdminUI();
                showToast("Modo Administrador activado");
            } else {
                showToast("Clave de administrador incorrecta", "error");
                inputAdminPin.value = '';
                inputAdminPin.focus();
            }
        });

        // Sistema de notificaciones Toast
        function showToast(message, type = 'success') {
            const toast = document.getElementById('toast');
            const toastMsg = document.getElementById('toast-message');
            const toastIconWrapper = document.getElementById('toast-icon-wrapper');

            toastMsg.textContent = message;
            if (type === 'error') {
                toastIconWrapper.innerHTML = `<i data-lucide="alert-triangle" class="w-5 h-5 text-red-400"></i>`;
            } else {
                toastIconWrapper.innerHTML = `<i data-lucide="check-circle" class="w-5 h-5 text-emerald-400"></i>`;
            }
            lucide.createIcons();

            toast.classList.remove('translate-y-20', 'opacity-0');
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 3500);
        }

        // 1. AUTENTICACIÓN OBLIGATORIA ANTES DE CONSULTAS
        async function initAuth() {
            try {
                if (typeof __initial_auth_token !== 'undefined' && __initial_auth_token) {
                    await signInWithCustomToken(auth, __initial_auth_token);
                } else {
                    await signInAnonymously(auth);
                }
            } catch (error) {
                console.error("Error en autenticación:", error);
                showToast("Error al conectar con el servidor", "error");
            }
        }

        onAuthStateChanged(auth, async (user) => {
            if (!user) return;
            currentUser = user;
            modalUserId.textContent = user.uid;

            updateAdminUI();

            // Solo cargar perfil y suscribirse a reportes si el usuario ya validó acceso
            if (hasTeamAccess || isAdmin) {
                await loadTechnicianProfile(user.uid);
                subscribeToReports();
            }
        });

        btnChangeUser.addEventListener('click', () => {
            inputUsername.value = technicianName;
            userModal.classList.remove('hidden');
        });

        // 2. MANEJO Y COMPRESIÓN DE IMÁGENES EN CANVAS
        function compressImage(file, maxWidth = 800, quality = 0.72) {
            return new Promise((resolve, reject) => {
                const reader = new FileReader();
                reader.readAsDataURL(file);
                reader.onload = (event) => {
                    const img = new Image();
                    img.src = event.target.result;
                    img.onload = () => {
                        const canvas = document.createElement('canvas');
                        let width = img.width;
                        let height = img.height;

                        if (width > maxWidth) {
                            height = Math.round((height * maxWidth) / width);
                            width = maxWidth;
                        }

                        canvas.width = width;
                        canvas.height = height;
                        const ctx = canvas.getContext('2d');
                        ctx.drawImage(img, 0, 0, width, height);

                        const dataUrl = canvas.toDataURL('image/jpeg', quality);
                        resolve(dataUrl);
                    };
                    img.onerror = (err) => reject(err);
                };
                reader.onerror = (err) => reject(err);
            });
        }

        dropZone.addEventListener('click', (e) => {
            if (e.target.closest('#btn-remove-photo')) return;
            photoInput.click();
        });

        photoInput.addEventListener('change', async (e) => {
            const file = e.target.files[0];
            if (!file) return;

            try {
                showToast("Procesando fotografía...");
                compressedImageDataUrl = await compressImage(file);
                imagePreview.src = compressedImageDataUrl;
                uploadPlaceholder.classList.add('hidden');
                imagePreviewContainer.classList.remove('hidden');
            } catch (error) {
                console.error("Error procesando imagen:", error);
                showToast("Error al procesar la imagen", "error");
            }
        });

        btnRemovePhoto.addEventListener('click', (e) => {
            e.stopPropagation();
            compressedImageDataUrl = null;
            photoInput.value = '';
            imagePreview.src = '';
            imagePreviewContainer.classList.add('hidden');
            uploadPlaceholder.classList.remove('hidden');
        });

        // 3. GUARDAR REPORTE EN FIRESTORE (RUTA PÚBLICA COMPARTIDA)
        maintenanceForm.addEventListener('submit', async (e) => {
            e.preventDefault();
            if (!currentUser) return;

            if (isAdmin) {
                showToast("Sal del Modo Administrador para cargar un reporte nuevo", "error");
                return;
            }

            if (!technicianName) {
                userModal.classList.remove('hidden');
                return;
            }

            if (!compressedImageDataUrl) {
                showToast("Por favor adjunta una fotografía del equipo", "error");
                return;
            }

            const equipment = document.getElementById('equipment-name').value.trim();
            const type = document.getElementById('maintenance-type').value;
            const status = document.getElementById('equipment-status').value;
            const description = document.getElementById('description').value.trim();

            btnSubmit.disabled = true;
            btnSubmit.innerHTML = `<span class="animate-spin rounded-full h-4 w-4 border-2 border-slate-900 border-t-transparent"></span><span>Guardando...</span>`;

            try {
                const now = new Date();
                const localDateISO = `${now.getFullYear()}-${String(now.getMonth() + 1).padStart(2, '0')}-${String(now.getDate()).padStart(2, '0')}`;

                const reportsCol = collection(db, 'artifacts', appId, 'public', 'data', 'maintenance_logs');
                await addDoc(reportsCol, {
                    equipment,
                    type,
                    status,
                    description,
                    photoUrl: compressedImageDataUrl,
                    technicianName,
                    authorUid: currentUser.uid,
                    timestamp: now.getTime(),
                    dateISO: localDateISO
                });

                maintenanceForm.reset();
                compressedImageDataUrl = null;
                imagePreviewContainer.classList.add('hidden');
                uploadPlaceholder.classList.remove('hidden');
                showToast("Reporte registrado correctamente");
            } catch (error) {
                console.error("Error al guardar reporte:", error);
                showToast("Error al guardar el reporte", "error");
            } finally {
                btnSubmit.disabled = false;
                btnSubmit.innerHTML = `<i data-lucide="send" class="w-4 h-4"></i><span>Guardar Reporte en Bitácora</span>`;
                lucide.createIcons();
            }
        });

        // 4. ESCUCHA EN TIEMPO REAL DE TODOS LOS REPORTES
        function subscribeToReports() {
            if (!currentUser || (!hasTeamAccess && !isAdmin)) return;
            if (typeof unsubscribeReports === 'function') {
                unsubscribeReports();
            }

            const reportsCol = collection(db, 'artifacts', appId, 'public', 'data', 'maintenance_logs');

            unsubscribeReports = onSnapshot(reportsCol, (snapshot) => {
                const items = [];
                snapshot.forEach((docSnap) => {
                    items.push({ id: docSnap.id, ...docSnap.data() });
                });

                items.sort((a, b) => (b.timestamp || 0) - (a.timestamp || 0));
                allReports = items;

                updateStats();
                renderReports();
            }, (error) => {
                console.error("Error en sincronización:", error);
                reportsContainer.innerHTML = `
                    <div class="bg-red-50 text-red-700 p-6 rounded-2xl border border-red-200 text-center">
                        <p class="font-semibold">Error de conexión con la base de datos</p>
                        <p class="text-xs mt-1">Verifica tu conexión e intenta recargar la página.</p>
                    </div>
                `;
            });
        }

        function updateStats() {
            const now = new Date();
            const todayISO = `${now.getFullYear()}-${String(now.getMonth() + 1).padStart(2, '0')}-${String(now.getDate()).padStart(2, '0')}`;

            const total = allReports.length;
            const todayCount = allReports.filter(r => r.dateISO === todayISO).length;
            const warningCount = allReports.filter(r => r.status !== 'Operativo').length;
            const uniqueUsers = new Set(allReports.map(r => r.technicianName)).size;

            document.getElementById('stat-total').textContent = total;
            document.getElementById('stat-today').textContent = todayCount;
            document.getElementById('stat-warning').textContent = warningCount;
            document.getElementById('stat-users').textContent = uniqueUsers;
        }

        function renderReports() {
            const searchTerm = filterSearch.value.toLowerCase().trim();
            const statusFilter = filterStatus.value;
            const dateFilter = filterDate.value;

            const filtered = allReports.filter(item => {
                const matchesSearch = !searchTerm || 
                    (item.equipment && item.equipment.toLowerCase().includes(searchTerm)) ||
                    (item.technicianName && item.technicianName.toLowerCase().includes(searchTerm)) ||
                    (item.description && item.description.toLowerCase().includes(searchTerm));

                const matchesStatus = statusFilter === 'ALL' || item.status === statusFilter;
                const matchesDate = !dateFilter || item.dateISO === dateFilter;

                return matchesSearch && matchesStatus && matchesDate;
            });

            if (filtered.length === 0) {
                reportsContainer.innerHTML = `
                    <div class="bg-white rounded-2xl p-10 text-center border border-slate-200/80">
                        <div class="w-12 h-12 rounded-full bg-slate-100 text-slate-400 flex items-center justify-center mx-auto mb-3">
                            <i data-lucide="folder-open" class="w-6 h-6"></i>
                        </div>
                        <h3 class="text-base font-semibold text-slate-800">No hay registros que mostrar</h3>
                        <p class="text-sm text-slate-500 mt-1">Completa el formulario para agregar el primer reporte diario o ajusta los filtros.</p>
                    </div>
                `;
                lucide.createIcons();
                return;
            }

            reportsContainer.innerHTML = filtered.map(report => {
                const dateObj = new Date(report.timestamp);
                const formattedDate = dateObj.toLocaleDateString('es-AR', { day: '2-digit', month: 'short', year: 'numeric' });
                const formattedTime = dateObj.toLocaleTimeString('es-AR', { hour: '2-digit', minute: '2-digit' });

                let statusBadge = '';
                if (report.status === 'Operativo') {
                    statusBadge = `<span class="inline-flex items-center gap-1 px-2.5 py-1 rounded-full text-xs font-semibold bg-emerald-50 text-emerald-700 border border-emerald-200"><span class="w-1.5 h-1.5 rounded-full bg-emerald-500"></span>Operativo</span>`;
                } else if (report.status === 'Observación') {
                    statusBadge = `<span class="inline-flex items-center gap-1 px-2.5 py-1 rounded-full text-xs font-semibold bg-amber-50 text-amber-700 border border-amber-200"><span class="w-1.5 h-1.5 rounded-full bg-amber-500"></span>En Observación</span>`;
                } else {
                    statusBadge = `<span class="inline-flex items-center gap-1 px-2.5 py-1 rounded-full text-xs font-semibold bg-red-50 text-red-700 border border-red-200"><span class="w-1.5 h-1.5 rounded-full bg-red-500"></span>Fuera de Servicio</span>`;
                }

                // Solo el Administrador con sesión activa puede borrar reportes
                const actionButtons = isAdmin ? `
                    <div class="flex items-center space-x-1">
                        <button onclick="window.promptDeleteReport('${report.id}')" class="text-slate-400 hover:text-red-600 p-1.5 rounded-lg hover:bg-red-50 transition cursor-pointer" title="Eliminar reporte por error">
                            <i data-lucide="trash-2" class="w-4 h-4"></i>
                        </button>
                    </div>
                ` : '';

                return `
                    <article class="bg-white rounded-2xl shadow-sm border border-slate-200/80 overflow-hidden animate-fade-in transition hover:shadow-md">
                        <div class="p-4 sm:p-5 flex flex-col sm:flex-row gap-4">
                            <!-- Miniatura Fotográfica -->
                            <div class="sm:w-44 sm:h-36 flex-shrink-0 relative group cursor-pointer rounded-xl overflow-hidden bg-slate-100"
                                 onclick="window.openLightbox('${report.id}')">
                                <img src="${report.photoUrl}" alt="${escapeHtml(report.equipment)}" 
                                     onerror="this.src='https://placehold.co/400x300/e2e8f0/64748b?text=Sin+Imagen'"
                                     class="w-full h-48 sm:h-full object-cover group-hover:scale-105 transition duration-300">
                                <div class="absolute inset-0 bg-slate-900/0 group-hover:bg-slate-900/30 transition flex items-center justify-center">
                                    <span class="opacity-0 group-hover:opacity-100 bg-white/90 text-slate-900 p-2 rounded-full shadow-md transition">
                                        <i data-lucide="maximize-2" class="w-4 h-4"></i>
                                    </span>
                                </div>
                            </div>

                            <!-- Contenido del Reporte -->
                            <div class="flex-grow flex flex-col justify-between">
                                <div>
                                    <div class="flex items-start justify-between gap-2">
                                        <div>
                                            <div class="flex flex-wrap items-center gap-2 mb-1">
                                                <span class="text-xs font-semibold uppercase tracking-wider text-amber-600 bg-amber-50 px-2 py-0.5 rounded-md">
                                                    ${escapeHtml(report.type || 'Mantenimiento')}
                                                </span>
                                                ${statusBadge}
                                            </div>
                                            <h3 class="text-base sm:text-lg font-bold text-slate-900 leading-snug">
                                                ${escapeHtml(report.equipment)}
                                            </h3>
                                        </div>
                                        ${actionButtons}
                                    </div>

                                        <p class="text-sm text-slate-600 mt-2 whitespace-pre-line leading-relaxed">
                                        ${escapeHtml(report.description)}
                                    </p>
                                </div>

                                <!-- Pie de tarjeta: Técnico y Fecha -->
                                <div class="mt-4 pt-3 border-t border-slate-100 flex flex-wrap items-center justify-between gap-2 text-xs text-slate-500">
                                    <div class="flex items-center space-x-2">
                                        <div class="w-6 h-6 rounded-full bg-slate-800 text-white flex items-center justify-center font-bold text-[11px]">
                                            ${escapeHtml((report.technicianName || 'U').charAt(0).toUpperCase())}
                                        </div>
                                        <span class="font-medium text-slate-700">${escapeHtml(report.technicianName || 'Técnico')}</span>
                                    </div>
                                    <div class="flex items-center space-x-1">
                                        <i data-lucide="clock" class="w-3.5 h-3.5 text-slate-400"></i>
                                        <span>${formattedDate} · ${formattedTime}</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </article>
                `;
            }).join('');

            lucide.createIcons();
        }

        function escapeHtml(str) {
            if (!str) return '';
            return String(str)
                .replace(/&/g, '&amp;')
                .replace(/</g, '&lt;')
                .replace(/>/g, '&gt;')
                .replace(/"/g, '&quot;')
                .replace(/'/g, '&#039;');
        }

        filterSearch.addEventListener('input', renderReports);
        filterStatus.addEventListener('change', renderReports);
        filterDate.addEventListener('change', renderReports);

        window.openLightbox = (reportId) => {
            const report = allReports.find(r => r.id === reportId);
            if (!report) return;
            document.getElementById('lightbox-img').src = report.photoUrl;
            document.getElementById('lightbox-title').textContent = `${report.equipment} (${report.status})`;
            document.getElementById('lightbox-desc').textContent = `${report.technicianName}: ${report.description}`;
            document.getElementById('lightbox-modal').classList.remove('hidden');
        };

        document.getElementById('close-lightbox').addEventListener('click', () => {
            document.getElementById('lightbox-modal').classList.add('hidden');
        });

        window.promptDeleteReport = (reportId) => {
            if (!isAdmin) {
                showToast("Solo el Administrador puede eliminar reportes", "error");
                return;
            }
            reportToDeleteId = reportId;
            document.getElementById('delete-modal').classList.remove('hidden');
        };

        document.getElementById('cancel-delete').addEventListener('click', () => {
            reportToDeleteId = null;
            document.getElementById('delete-modal').classList.add('hidden');
        });

        document.getElementById('confirm-delete').addEventListener('click', async () => {
            if (!reportToDeleteId || !currentUser || !isAdmin) return;
            try {
                const docRef = doc(db, 'artifacts', appId, 'public', 'data', 'maintenance_logs', reportToDeleteId);
                await deleteDoc(docRef);
                showToast("Reporte eliminado");
            } catch (error) {
                console.error("Error al eliminar:", error);
                showToast("No se pudo eliminar el reporte", "error");
            } finally {
                reportToDeleteId = null;
                document.getElementById('delete-modal').classList.add('hidden');
            }
        });

        initAuth();
    </script>
</body>
</html>
