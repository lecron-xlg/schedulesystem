<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>检查预约管理系统（带备注记忆和工作量统计）</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f5f7fa;
            margin: 0;
            padding: 20px;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        header {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            padding: 20px;
            text-align: center;
        }

        h1 {
            margin: 0;
            font-size: 2em;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            padding: 20px;
        }

        .form-section {
            flex: 1;
            min-width: 300px;
            padding: 20px;
            border-right: 1px solid #eee;
        }

        .list-section {
            flex: 2;
            min-width: 500px;
            padding: 20px;
        }

        h2 {
            color: #2c3e50;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
            margin-top: 0;
        }

        .form-group {
            margin-bottom: 15px;
            position: relative;
        }

        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        input, select, textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }

        .autocomplete-items {
            position: absolute;
            border: 1px solid #d4d4d4;
            border-bottom: none;
            border-top: none;
            z-index: 99;
            top: 100%;
            left: 0;
            right: 0;
            max-height: 200px;
            overflow-y: auto;
            background-color: #fff;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .autocomplete-items div {
            padding: 10px;
            cursor: pointer;
            border-bottom: 1px solid #d4d4d4;
        }

        .autocomplete-items div:hover {
            background-color: #e9e9e9;
        }

        .autocomplete-active {
            background-color: #3498db !important;
            color: #ffffff;
        }

        button {
            background: linear-gradient(to right, #3498db, #2c3e50);
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            width: 100%;
            transition: background 0.3s ease;
            margin-top: 10px;
        }

        button:hover {
            background: linear-gradient(to right, #2980b9, #1a2530);
        }

        #cancelEditBtn {
            background: linear-gradient(to right, #95a5a6, #7f8c8d);
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            font-size: 0.9em;
        }

        th, td {
            padding: 12px 8px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

        th {
            background-color: #f8f9fa;
            color: #2c3e50;
            font-weight: bold;
            white-space: nowrap;
            cursor: pointer;
            user-select: none; /* 防止文本选中 */
            position: relative; /* 用于定位排序图标 */
        }

        th:hover {
            background-color: #e9ecef;
        }

        tr:hover {
            background-color: #f1f7fd;
        }

        .status-badge {
            padding: 4px 8px;
            border-radius: 12px;
            font-size: 0.85em;
            font-weight: bold;
        }

        .status-pending { background-color: #fff3cd; color: #856404; }
        .status-confirmed { background-color: #d4edda; color: #155724; }
        .status-completed { background-color: #cce5ff; color: #004085; }
        .status-cancelled { background-color: #f8d7da; color: #721c24; }

        .action-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 5px;
        }

        .action-btn {
            padding: 5px 10px;
            font-size: 0.8em;
            width: auto;
        }

        .filter-section {
            margin-bottom: 20px;
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            align-items: end;
        }

        .filter-group {
            flex: 1;
            min-width: 150px;
        }

        .search-group {
            flex: 2;
            min-width: 200px;
        }

        footer {
            text-align: center;
            padding: 20px;
            color: #7f8c8d;
            font-size: 0.9em;
            border-top: 1px solid #eee;
        }

        .no-results {
            text-align: center;
            color: #7f8c8d;
            font-style: italic;
            padding: 20px;
        }

        /* 排序图标样式 */
        .sort-icon {
            position: absolute;
            right: 8px;
            top: 50%;
            transform: translateY(-50%);
            opacity: 0.5;
            font-size: 0.8em;
        }
        .sort-icon.active {
            opacity: 1;
            color: #3498db;
        }

        /* 统计区域样式 */
        .stats-section {
            background-color: #f8f9fa;
            border: 1px solid #e9ecef;
            border-radius: 5px;
            padding: 15px;
            margin-bottom: 20px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
        }

        .stats-title {
            font-weight: bold;
            margin-bottom: 10px;
            color: #2c3e50;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .stats-controls {
            display: flex;
            gap: 10px;
            align-items: center;
        }

        .stats-period-btn {
            background: #e9ecef;
            color: #495057;
            border: 1px solid #ced4da;
            padding: 5px 10px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.85em;
        }

        .stats-period-btn.active {
            background: #3498db;
            color: white;
            border-color: #3498db;
        }

        .stats-display {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }

        .stat-item {
            flex: 1;
            min-width: 120px;
            text-align: center;
        }

        .stat-value {
            font-size: 1.8em;
            font-weight: bold;
            color: #3498db;
        }

        .stat-label {
            font-size: 0.9em;
            color: #6c757d;
        }

        /* 复制成功提示 */
        .copy-notification {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border-radius: 4px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s ease-in-out;
        }
        .copy-notification.show {
            opacity: 1;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            .form-section {
                border-right: none;
                border-bottom: 1px solid #eee;
            }
            table {
                font-size: 0.8em;
            }
            th, td {
                padding: 8px 4px;
            }
            .filter-section {
                flex-direction: column;
                align-items: stretch;
            }
            .stats-display {
                flex-direction: column;
                gap: 10px;
            }
            .stat-item {
                min-width: auto;
            }
        }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>🏥 凯威电生理预约管理系统 (V2)</h1>
        <p>高效预约管理/工作量统计</p>
    </header>

    <div class="main-content">
        <div class="form-section">
            <h2>📝 添加/编辑预约</h2>
            <form id="appointmentForm">
                <input type="hidden" id="editId">
                <div class="form-group">
                    <label for="patientName">患者姓名:</label>
                    <input type="text" id="patientName" required placeholder="请输入患者姓名">
                </div>
                <div class="form-group">
                    <label for="medicalRecordNumber">诊疗号:</label>
                    <input type="text" id="medicalRecordNumber" required placeholder="请输入诊疗号">
                </div>
                <div class="form-group">
                    <label for="department">科室:</label>
                    <input type="text" id="department" required placeholder="请输入或选择科室">
                </div>
                <div class="form-group">
                    <label for="checkupItem">检查项目:</label>
                    <input type="text" id="checkupItem" required placeholder="请输入或选择检查项目">
                </div>
                <div class="form-group">
                    <label for="doctor">操作医生:</label>
                    <input type="text" id="doctor" required placeholder="请输入或选择医生">
                </div>
                <div class="form-group">
                    <label for="appointmentTime">预约时间:</label>
                    <input type="datetime-local" id="appointmentTime" required>
                </div>
                <div class="form-group">
                    <label for="status">检查状态:</label>
                    <select id="status" required>
                        <option value="待确认">待确认</option>
                        <option value="已确认">已确认</option>
                        <option value="已完成">已完成</option>
                        <option value="已取消">已取消</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="notes">备注:</label>
                    <textarea id="notes" rows="2" placeholder="请输入备注信息"></textarea>
                </div>
                <button type="submit" id="saveBtn">💾 保存预约</button>
                <button type="button" id="cancelEditBtn" style="display:none;">↩️ 取消编辑</button>
            </form>
        </div>

        <div class="list-section">
            <h2>📋 预约列表</h2>
            
            <!-- 工作量统计区域 -->
            <div class="stats-section">
                <div class="stats-title">
                    <span>📊 预约工作量统计</span>
                    <div class="stats-controls">
                        <button class="stats-period-btn active" data-period="week">本周</button>
                        <button class="stats-period-btn" data-period="month">本月</button>
                        <button class="stats-period-btn" data-period="quarter">本季度</button>
                        <button class="stats-period-btn" data-period="year">本年</button>
                    </div>
                </div>
                <div class="stats-display">
                    <div class="stat-item">
                        <div class="stat-value" id="totalAppointments">0</div>
                        <div class="stat-label">总预约数</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value" id="confirmedAppointments">0</div>
                        <div class="stat-label">已确认</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value" id="completedAppointments">0</div>
                        <div class="stat-label">已完成</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value" id="pendingAppointments">0</div>
                        <div class="stat-label">待确认</div>
                    </div>
                </div>
            </div>

            <div class="filter-section">
                <div class="filter-group">
                    <label for="filterStatus">状态:</label>
                    <select id="filterStatus">
                        <option value="">全部</option>
                        <option value="待确认">待确认</option>
                        <option value="已确认">已确认</option>
                        <option value="已完成">已完成</option>
                        <option value="已取消">已取消</option>
                    </select>
                </div>
                <div class="filter-group">
                    <label for="filterDepartment">科室:</label>
                    <select id="filterDepartment">
                        <option value="">全部</option>
                    </select>
                </div>
                <div class="filter-group">
                    <label for="filterDoctor">医生:</label>
                    <select id="filterDoctor">
                        <option value="">全部</option>
                    </select>
                </div>
                <div class="search-group">
                    <label for="searchPatient">搜索患者 (姓名或诊疗号):</label>
                    <div style="display: flex; gap: 5px;">
                        <input type="text" id="searchPatient" placeholder="输入姓名或诊疗号">
                        <button type="button" id="searchBtn" style="width: auto; padding: 10px 15px;">🔍</button>
                        <button type="button" id="clearSearchBtn" style="width: auto; padding: 10px 15px; background: #95a5a6;">🗑️</button>
                    </div>
                </div>
            </div>

            <div style="overflow-x: auto;">
                <table id="appointmentsTable">
                    <thead>
                        <tr>
                            <th onclick="sortTable('patient')">患者<br>(诊疗号) <span class="sort-icon" id="sort-patient">↕️</span></th>
                            <th onclick="sortTable('department')">科室 <span class="sort-icon" id="sort-department">↕️</span></th>
                            <th onclick="sortTable('checkupItem')">项目 <span class="sort-icon" id="sort-checkupItem">↕️</span></th>
                            <th onclick="sortTable('doctor')">医生 <span class="sort-icon" id="sort-doctor">↕️</span></th>
                            <th onclick="sortTable('time')">时间 <span class="sort-icon" id="sort-time">↕️</span></th>
                            <th onclick="sortTable('status')">状态 <span class="sort-icon" id="sort-status">↕️</span></th>
                            <th>操作</th>
                        </tr>
                    </thead>
                    <tbody>
                        <!-- 数据将通过JavaScript动态生成 -->
                    </tbody>
                </table>
            </div>
        </div>
    </div>

    <!-- 复制成功提示 -->
    <div id="copyNotification" class="copy-notification">📋 信息已复制到剪贴板</div>

    <footer>
        <p>&copy; 2023 检查预约管理系统. All rights reserved.</p>
    </footer>
</div>

<script>
    // 清空初始数据和记忆数据
    let appointments = [];
    let departmentsMemory = [];
    let medicalRecordNumbersMemory = [];
    let checkupItemsMemory = [];
    let doctorsMemory = [];
    let notesMemory = []; // 新增：备注记忆
    
    let nextId = 1; // 重置ID计数器
    let isEditing = false;
    let currentEditId = null;

    // 排序状态
    let sortState = {
        key: null, // 'time', 'patient', 'department', 'checkupItem', 'doctor', 'status'
        direction: 'asc' // 'asc' or 'desc'
    };

    // 当前统计周期
    let currentStatsPeriod = 'week';

    // DOM元素
    const form = document.getElementById('appointmentForm');
    const editIdInput = document.getElementById('editId');
    const patientNameInput = document.getElementById('patientName');
    const medicalRecordNumberInput = document.getElementById('medicalRecordNumber');
    const departmentInput = document.getElementById('department');
    const checkupItemInput = document.getElementById('checkupItem');
    const doctorInput = document.getElementById('doctor');
    const appointmentTimeInput = document.getElementById('appointmentTime');
    const statusSelect = document.getElementById('status');
    const notesTextarea = document.getElementById('notes');
    const cancelEditBtn = document.getElementById('cancelEditBtn');
    const tableBody = document.querySelector('#appointmentsTable tbody');
    const filterStatusSelect = document.getElementById('filterStatus');
    const filterDepartmentSelect = document.getElementById('filterDepartment');
    const filterDoctorSelect = document.getElementById('filterDoctor');
    const searchPatientInput = document.getElementById('searchPatient');
    const searchBtn = document.getElementById('searchBtn');
    const clearSearchBtn = document.getElementById('clearSearchBtn');
    const copyNotification = document.getElementById('copyNotification'); // 新增：复制提示元素

    // 统计相关DOM元素
    const statsPeriodButtons = document.querySelectorAll('.stats-period-btn');
    const totalAppointmentsEl = document.getElementById('totalAppointments');
    const confirmedAppointmentsEl = document.getElementById('confirmedAppointments');
    const completedAppointmentsEl = document.getElementById('completedAppointments');
    const pendingAppointmentsEl = document.getElementById('pendingAppointments');

    // 初始化
    document.addEventListener('DOMContentLoaded', () => {
        loadFromLocalStorage();
        renderAppointments(); // 初始渲染所有数据
        updateStats(); // 初始更新统计
        setupEventListeners();
        initAutocomplete(medicalRecordNumberInput, medicalRecordNumbersMemory);
        initAutocomplete(departmentInput, departmentsMemory);
        initAutocomplete(checkupItemInput, checkupItemsMemory);
        initAutocomplete(doctorInput, doctorsMemory);
        // 新增：为备注框初始化自动完成
        initAutocomplete(notesTextarea, notesMemory);
        populateFilters();
    });

    // 从本地存储加载数据
    function loadFromLocalStorage() {
        const savedDepartments = localStorage.getItem('departmentsMemory');
        const savedMRNs = localStorage.getItem('medicalRecordNumbersMemory');
        const savedCheckups = localStorage.getItem('checkupItemsMemory');
        const savedDoctors = localStorage.getItem('doctorsMemory');
        const savedNotes = localStorage.getItem('notesMemory'); // 新增
        const savedAppointments = localStorage.getItem('appointments');
        
        if (savedDepartments) departmentsMemory = JSON.parse(savedDepartments);
        if (savedMRNs) medicalRecordNumbersMemory = JSON.parse(savedMRNs);
        if (savedCheckups) checkupItemsMemory = JSON.parse(savedCheckups);
        if (savedDoctors) doctorsMemory = JSON.parse(savedDoctors);
        if (savedNotes) notesMemory = JSON.parse(savedNotes); // 新增
        if (savedAppointments) {
            appointments = JSON.parse(savedAppointments);
            if (appointments.length > 0) {
                nextId = Math.max(...appointments.map(a => a.id)) + 1;
            }
        }
    }

    // 保存到本地存储
    function saveToLocalStorage() {
        localStorage.setItem('departmentsMemory', JSON.stringify(departmentsMemory));
        localStorage.setItem('medicalRecordNumbersMemory', JSON.stringify(medicalRecordNumbersMemory));
        localStorage.setItem('checkupItemsMemory', JSON.stringify(checkupItemsMemory));
        localStorage.setItem('doctorsMemory', JSON.stringify(doctorsMemory));
        localStorage.setItem('notesMemory', JSON.stringify(notesMemory)); // 新增
        localStorage.setItem('appointments', JSON.stringify(appointments));
    }

    // 设置事件监听器
    function setupEventListeners() {
        form.addEventListener('submit', handleFormSubmit);
        cancelEditBtn.addEventListener('click', cancelEdit);
        filterStatusSelect.addEventListener('change', () => { renderAppointments(); updateStats(); });
        filterDepartmentSelect.addEventListener('change', () => { renderAppointments(); updateStats(); });
        filterDoctorSelect.addEventListener('change', () => { renderAppointments(); updateStats(); });
        
        searchBtn.addEventListener('click', () => {
             renderAppointments();
             updateStats(); // 搜索时也更新统计
        });
        clearSearchBtn.addEventListener('click', () => {
             searchPatientInput.value = '';
             renderAppointments();
             updateStats(); // 清除搜索时也更新统计
        });
        
        searchPatientInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                 renderAppointments();
                 updateStats(); // 搜索时也更新统计
            }
        });

        // 统计周期按钮事件
        statsPeriodButtons.forEach(button => {
            button.addEventListener('click', () => {
                statsPeriodButtons.forEach(btn => btn.classList.remove('active'));
                button.classList.add('active');
                currentStatsPeriod = button.dataset.period;
                updateStats();
            });
        });
    }

    // 处理表单提交
    function handleFormSubmit(e) {
        e.preventDefault(); // 阻止默认提交行为
        
        const appointment = {
            id: isEditing ? currentEditId : nextId++,
            patientName: patientNameInput.value.trim(),
            medicalRecordNumber: medicalRecordNumberInput.value.trim(),
            department: departmentInput.value.trim(),
            checkupItem: checkupItemInput.value.trim(),
            doctor: doctorInput.value.trim(),
            appointmentTime: appointmentTimeInput.value,
            status: statusSelect.value,
            notes: notesTextarea.value.trim()
        };

        // 验证必填字段
        if (!appointment.patientName || !appointment.medicalRecordNumber || !appointment.department || 
            !appointment.checkupItem || !appointment.doctor || !appointment.appointmentTime) {
            alert("请填写所有必填字段！");
            return;
        }

        // 更新记忆库
        if (appointment.medicalRecordNumber && !medicalRecordNumbersMemory.includes(appointment.medicalRecordNumber)) {
            medicalRecordNumbersMemory.push(appointment.medicalRecordNumber);
        }
        if (appointment.department && !departmentsMemory.includes(appointment.department)) {
            departmentsMemory.push(appointment.department);
        }
        if (appointment.checkupItem && !checkupItemsMemory.includes(appointment.checkupItem)) {
            checkupItemsMemory.push(appointment.checkupItem);
        }
        if (appointment.doctor && !doctorsMemory.includes(appointment.doctor)) {
            doctorsMemory.push(appointment.doctor);
        }
        // 新增：更新备注记忆库
        if (appointment.notes && !notesMemory.includes(appointment.notes)) {
            notesMemory.push(appointment.notes);
        }

        if (isEditing) {
            const index = appointments.findIndex(a => a.id === currentEditId);
            if (index !== -1) {
                appointments[index] = appointment;
            }
            isEditing = false;
            currentEditId = null;
            cancelEditBtn.style.display = 'none';
        } else {
            appointments.push(appointment);
        }

        saveToLocalStorage();
        renderAppointments(); // 保存后重新渲染
        updateStats(); // 保存后更新统计
        populateFilters();
        form.reset();
    }

    // 编辑预约
    function editAppointment(id) {
        const appointment = appointments.find(a => a.id === id);
        if (appointment) {
            patientNameInput.value = appointment.patientName;
            medicalRecordNumberInput.value = appointment.medicalRecordNumber;
            departmentInput.value = appointment.department;
            checkupItemInput.value = appointment.checkupItem;
            doctorInput.value = appointment.doctor;
            appointmentTimeInput.value = appointment.appointmentTime;
            statusSelect.value = appointment.status;
            notesTextarea.value = appointment.notes || '';
            
            isEditing = true;
            currentEditId = id;
            cancelEditBtn.style.display = 'block';
            
            document.querySelector('.form-section').scrollIntoView({ behavior: 'smooth' });
        }
    }

    // 取消编辑
    function cancelEdit() {
        form.reset();
        isEditing = false;
        currentEditId = null;
        cancelEditBtn.style.display = 'none';
    }

    // 删除预约
    function deleteAppointment(id) {
        if (confirm('确定要删除这个预约吗?')) {
            appointments = appointments.filter(a => a.id !== id);
            saveToLocalStorage();
            renderAppointments(); // 删除后重新渲染
            updateStats(); // 删除后更新统计
            populateFilters();
        }
    }

    // 更新状态
    function updateStatus(id, newStatus) {
        const appointment = appointments.find(a => a.id === id);
        if (appointment) {
            appointment.status = newStatus;
            saveToLocalStorage();
            renderAppointments(); // 状态更新后重新渲染
            updateStats(); // 状态更新后更新统计
        }
    }

    // 排序函数
    function sortTable(key) {
        // 如果点击的是当前排序的列，则切换方向
        if (sortState.key === key) {
            sortState.direction = sortState.direction === 'asc' ? 'desc' : 'asc';
        } else {
            // 否则，按新列升序排序
            sortState.key = key;
            sortState.direction = 'asc';
        }
        updateSortIcons(); // 更新UI图标
        renderAppointments(); // 重新渲染以应用排序
    }

    // 更新排序图标
    function updateSortIcons() {
        // 重置所有图标
        document.querySelectorAll('.sort-icon').forEach(icon => {
            icon.textContent = '↕️';
            icon.classList.remove('active');
        });

        // 设置当前排序列的图标
        if (sortState.key) {
            const currentIcon = document.getElementById(`sort-${sortState.key}`);
            if (currentIcon) {
                currentIcon.textContent = sortState.direction === 'asc' ? '↑' : '↓';
                currentIcon.classList.add('active');
            }
        }
    }

    // 渲染预约列表 (核心过滤和排序逻辑)
    function renderAppointments() {
        // 获取所有过滤条件
        const filterStatus = filterStatusSelect.value.trim();
        const filterDepartment = filterDepartmentSelect.value.trim();
        const filterDoctor = filterDoctorSelect.value.trim();
        const searchTerm = searchPatientInput.value ? searchPatientInput.value.toLowerCase().trim() : '';

        // 应用过滤器
        let filteredAppointments = appointments.filter(app => {
            const matchesStatus = !filterStatus || app.status === filterStatus;
            const matchesDepartment = !filterDepartment || app.department === filterDepartment;
            const matchesDoctor = !filterDoctor || app.doctor === filterDoctor;
            const matchesSearch = !searchTerm || 
                (app.patientName && app.patientName.toLowerCase().includes(searchTerm)) || 
                (app.medicalRecordNumber && app.medicalRecordNumber.toLowerCase().includes(searchTerm));

            return matchesStatus && matchesDepartment && matchesDoctor && matchesSearch;
        });

        // 应用排序
        if (sortState.key) {
            filteredAppointments.sort((a, b) => {
                let valA, valB;

                switch(sortState.key) {
                    case 'time':
                        valA = a.appointmentTime;
                        valB = b.appointmentTime;
                        break;
                    case 'patient':
                        valA = a.patientName ? a.patientName.toLowerCase() : '';
                        valB = b.patientName ? b.patientName.toLowerCase() : '';
                        break;
                    case 'department':
                        valA = a.department ? a.department.toLowerCase() : '';
                        valB = b.department ? b.department.toLowerCase() : '';
                        break;
                    case 'checkupItem':
                        valA = a.checkupItem ? a.checkupItem.toLowerCase() : '';
                        valB = b.checkupItem ? b.checkupItem.toLowerCase() : '';
                        break;
                    case 'doctor':
                        valA = a.doctor ? a.doctor.toLowerCase() : '';
                        valB = b.doctor ? b.doctor.toLowerCase() : '';
                        break;
                    case 'status':
                        valA = a.status ? a.status.toLowerCase() : '';
                        valB = b.status ? b.status.toLowerCase() : '';
                        break;
                    default:
                        return 0;
                }

                if (valA < valB) {
                    return sortState.direction === 'asc' ? -1 : 1;
                }
                if (valA > valB) {
                    return sortState.direction === 'asc' ? 1 : -1;
                }
                return 0;
            });
        }

        // 渲染表格
        tableBody.innerHTML = '';

        if (filteredAppointments.length === 0) {
            const noResultsRow = document.createElement('tr');
            const noResultsCell = document.createElement('td');
            noResultsCell.colSpan = 7;
            noResultsCell.className = 'no-results';
            noResultsCell.textContent = '未找到匹配的预约记录。';
            noResultsRow.appendChild(noResultsCell);
            tableBody.appendChild(noResultsRow);
            return;
        }

        filteredAppointments.forEach(app => {
            const row = document.createElement('tr');
            const formattedTime = new Date(app.appointmentTime).toLocaleString('zh-CN', {
                year: 'numeric', month: '2-digit', day: '2-digit',
                hour: '2-digit', minute: '2-digit'
            });

            // 构建要复制的文本
            const copyText = `患者姓名: ${app.patientName}\n诊疗号: ${app.medicalRecordNumber}\n科室: ${app.department}\n检查项目: ${app.checkupItem}\n操作医生: ${app.doctor}\n预约时间: ${formattedTime}\n检查状态: ${app.status}\n备注: ${app.notes || '无'}`;

            row.innerHTML = `
                <td>${app.patientName}<br><small>${app.medicalRecordNumber}</small></td>
                <td>${app.department}</td>
                <td>${app.checkupItem}</td>
                <td>👨‍⚕️ ${app.doctor}</td>
                <td>${formattedTime}</td>
                <td><span class="status-badge status-${app.status === '待确认' ? 'pending' : app.status === '已确认' ? 'confirmed' : app.status === '已完成' ? 'completed' : 'cancelled'}">${app.status}</span></td>
                <td class="action-buttons">
                    <button class="action-btn" onclick="copyPatientInfo(${app.id})" title="复制信息">📋</button>
                    <button class="action-btn" onclick="editAppointment(${app.id})" title="编辑">✏️</button>
                    <button class="action-btn" onclick="deleteAppointment(${app.id})" title="删除">🗑️</button>
                    <select onchange="updateStatus(${app.id}, this.value)" title="更改状态">
                        <option value="${app.status}" selected>${app.status}</option>
                        <option value="待确认">待确认</option>
                        <option value="已确认">已确认</option>
                        <option value="已完成">已完成</option>
                        <option value="已取消">已取消</option>
                    </select>
                </td>
            `;
            tableBody.appendChild(row);
        });
    }

    // 新增：复制病人信息到剪贴板
    async function copyPatientInfo(id) {
        const appointment = appointments.find(a => a.id === id);
        if (!appointment) return;

        const formattedTime = new Date(appointment.appointmentTime).toLocaleString('zh-CN', {
            year: 'numeric', month: '2-digit', day: '2-digit',
            hour: '2-digit', minute: '2-digit'
        });

        const textToCopy = `患者姓名: ${appointment.patientName}\n诊疗号: ${appointment.medicalRecordNumber}\n科室: ${appointment.department}\n检查项目: ${appointment.checkupItem}\n操作医生: ${appointment.doctor}\n预约时间: ${formattedTime}\n检查状态: ${appointment.status}\n备注: ${appointment.notes || '无'}`;

        try {
            await navigator.clipboard.writeText(textToCopy);
            // 显示提示
            copyNotification.classList.add('show');
            setTimeout(() => {
                copyNotification.classList.remove('show');
            }, 2000); // 2秒后隐藏
        } catch (err) {
            console.error('复制失败: ', err);
            alert('复制失败，请手动选择复制。');
        }
    }

    // 计算统计日期范围
    function getStatsDateRange(period) {
        const now = new Date();
        let start, end;

        switch(period) {
            case 'week':
                // 本周一到周日
                const dayOfWeek = now.getDay(); // 0 (Sunday) to 6 (Saturday)
                const diffToMonday = dayOfWeek === 0 ? -6 : 1 - dayOfWeek; // Adjust if Sunday
                start = new Date(now);
                start.setDate(now.getDate() + diffToMonday);
                start.setHours(0, 0, 0, 0);

                end = new Date(start);
                end.setDate(start.getDate() + 6);
                end.setHours(23, 59, 59, 999);
                break;
            case 'month':
                // 本月1号到月末
                start = new Date(now.getFullYear(), now.getMonth(), 1);
                end = new Date(now.getFullYear(), now.getMonth() + 1, 0);
                end.setHours(23, 59, 59, 999);
                break;
            case 'quarter':
                // 当前季度
                const quarter = Math.floor(now.getMonth() / 3);
                start = new Date(now.getFullYear(), quarter * 3, 1);
                end = new Date(start.getFullYear(), start.getMonth() + 3, 0);
                end.setHours(23, 59, 59, 999);
                break;
            case 'year':
                // 今年1月1号到12月31号
                start = new Date(now.getFullYear(), 0, 1);
                end = new Date(now.getFullYear(), 11, 31);
                end.setHours(23, 59, 59, 999);
                break;
            default:
                start = new Date(0);
                end = new Date();
        }
        return { start, end };
    }

    // 更新统计信息
    function updateStats() {
         // 首先获取当前过滤和搜索后的预约列表
        const filterStatus = filterStatusSelect.value.trim();
        const filterDepartment = filterDepartmentSelect.value.trim();
        const filterDoctor = filterDoctorSelect.value.trim();
        const searchTerm = searchPatientInput.value ? searchPatientInput.value.toLowerCase().trim() : '';

        let filteredAppointmentsForStats = appointments.filter(app => {
            const matchesStatus = !filterStatus || app.status === filterStatus;
            const matchesDepartment = !filterDepartment || app.department === filterDepartment;
            const matchesDoctor = !filterDoctor || app.doctor === filterDoctor;
            const matchesSearch = !searchTerm || 
                (app.patientName && app.patientName.toLowerCase().includes(searchTerm)) || 
                (app.medicalRecordNumber && app.medicalRecordNumber.toLowerCase().includes(searchTerm));
            return matchesStatus && matchesDepartment && matchesDoctor && matchesSearch;
        });

        // 获取当前周期的日期范围
        const { start, end } = getStatsDateRange(currentStatsPeriod);
        
        // 过滤出在该日期范围内的预约
        const appointmentsInRange = filteredAppointmentsForStats.filter(app => {
            const appDate = new Date(app.appointmentTime);
            return appDate >= start && appDate <= end;
        });

        // 计算统计数据
        const total = appointmentsInRange.length;
        const confirmed = appointmentsInRange.filter(a => a.status === '已确认').length;
        const completed = appointmentsInRange.filter(a => a.status === '已完成').length;
        const pending = appointmentsInRange.filter(a => a.status === '待确认').length;

        // 更新UI
        totalAppointmentsEl.textContent = total;
        confirmedAppointmentsEl.textContent = confirmed;
        completedAppointmentsEl.textContent = completed;
        pendingAppointmentsEl.textContent = pending;
    }


    // 填充筛选下拉框
    function populateFilters() {
        const selectedDept = filterDepartmentSelect.value;
        const selectedDoc = filterDoctorSelect.value;

        filterDepartmentSelect.innerHTML = '<option value="">全部</option>';
        const uniqueDepartments = [...new Set(appointments.map(a => a.department))];
        uniqueDepartments.forEach(dept => {
            const option = document.createElement('option');
            option.value = dept;
            option.textContent = dept;
            if (dept === selectedDept) option.selected = true;
            filterDepartmentSelect.appendChild(option);
        });

        filterDoctorSelect.innerHTML = '<option value="">全部</option>';
        const uniqueDoctors = [...new Set(appointments.map(a => a.doctor))];
        uniqueDoctors.forEach(doc => {
            const option = document.createElement('option');
            option.value = doc;
            option.textContent = doc;
            if (doc === selectedDoc) option.selected = true;
            filterDoctorSelect.appendChild(option);
        });
    }

    // 初始化自动完成 (通用函数)
    function initAutocomplete(inputElement, memoryArray) {
        let currentFocus;
        
        inputElement.addEventListener("input", function(e) {
            let val = this.value;
            closeAllLists();
            if (!val) { return false;}
            currentFocus = -1;
            
            let autocompleteList = document.createElement("DIV");
            autocompleteList.setAttribute("id", this.id + "-autocomplete-list");
            autocompleteList.setAttribute("class", "autocomplete-items");
            this.parentNode.appendChild(autocompleteList);
            
            let matches = 0;
            memoryArray.forEach(item => {
                if (matches >= 5 && val.length > 1) return;
                if (item.substr(0, val.length).toUpperCase() == val.toUpperCase()) {
                    matches++;
                    let suggestionItem = document.createElement("DIV");
                    suggestionItem.innerHTML = "<strong>" + item.substr(0, val.length) + "</strong>";
                    suggestionItem.innerHTML += item.substr(val.length);
                    suggestionItem.innerHTML += "<input type='hidden' value='" + item + "'>";
                    suggestionItem.addEventListener("click", function(e) {
                        inputElement.value = this.getElementsByTagName("input")[0].value;
                        closeAllLists();
                    });
                    autocompleteList.appendChild(suggestionItem);
                }
            });
        });

        inputElement.addEventListener("keydown", function(e) {
            let list = document.getElementById(this.id + "-autocomplete-list");
            if (list) list = list.getElementsByTagName("div");
            if (e.keyCode == 40) {
                currentFocus++;
                addActive(list);
            } else if (e.keyCode == 38) {
                currentFocus--;
                addActive(list);
            } else if (e.keyCode == 13) {
                e.preventDefault();
                if (currentFocus > -1 && list) {
                    list[currentFocus].click();
                }
            }
        });

        function addActive(list) {
            if (!list) return false;
            removeActive(list);
            if (currentFocus >= list.length) currentFocus = 0;
            if (currentFocus < 0) currentFocus = (list.length - 1);
            list[currentFocus].classList.add("autocomplete-active");
        }

        function removeActive(list) {
            for (let i = 0; i < list.length; i++) {
                list[i].classList.remove("autocomplete-active");
            }
        }

        function closeAllLists(elmnt) {
            let autocompleteItems = document.getElementsByClassName("autocomplete-items");
            for (let i = 0; i < autocompleteItems.length; i++) {
                if (elmnt != autocompleteItems[i] && elmnt != inputElement) {
                    autocompleteItems[i].parentNode.removeChild(autocompleteItems[i]);
                }
            }
        }

        document.addEventListener("click", function (e) {
            closeAllLists(e.target);
        });
    }

    // 暴露全局函数供HTML调用
    window.editAppointment = editAppointment;
    window.deleteAppointment = deleteAppointment;
    window.updateStatus = updateStatus;
    window.sortTable = sortTable;
    window.copyPatientInfo = copyPatientInfo; // 新增
</script>

</body>
</html>
