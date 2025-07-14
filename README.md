<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IT120 - Network Essentials - Comptia Network+ </title>
    <style>
        :root {
            --primary-blue: #1e3a8a;
            --secondary-blue: #3b82f6;
            --accent-blue: #60a5fa;
            --light-blue: #dbeafe;
            --text-dark: #1f2937;
            --text-light: #6b7280;
            --background: #f8fafc;
            --white: #ffffff;
            --border: #e5e7eb;
            --success: #10b981;
            --warning: #f59e0b;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--background);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            color: white;
            padding: 30px 0;
            text-align: center;
            margin-bottom: 30px;
            border-radius: 10px;
        }

        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .header p {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        .title-bar {
            background: var(--white);
            border: 2px solid var(--primary-blue);
            border-radius: 10px;
            padding: 25px;
            margin-bottom: 30px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .title-bar h2 {
            color: var(--primary-blue);
            margin-bottom: 20px;
            font-size: 1.8rem;
            border-bottom: 2px solid var(--accent-blue);
            padding-bottom: 10px;
        }

        .instructor-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .info-group {
            background: var(--light-blue);
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid var(--primary-blue);
        }

        .info-group label {
            display: block;
            font-weight: 600;
            color: var(--primary-blue);
            margin-bottom: 5px;
        }

        .info-group input, .info-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid var(--border);
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .info-group input:focus, .info-group textarea:focus {
            outline: none;
            border-color: var(--secondary-blue);
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
        }

        .course-section {
            background: var(--white);
            margin-bottom: 30px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .section-header {
            background: var(--primary-blue);
            color: white;
            padding: 20px;
            position: relative;
        }

        .section-header h3 {
            font-size: 1.5rem;
            margin-bottom: 5px;
        }

        .section-header p {
            opacity: 0.9;
        }

        .edit-btn {
            position: absolute;
            top: 15px;
            right: 20px;
            background: var(--accent-blue);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 0.9rem;
            transition: background-color 0.3s;
        }

        .edit-btn:hover {
            background: var(--secondary-blue);
        }

        .edit-btn:disabled {
            background: var(--text-light);
            cursor: not-allowed;
        }

        .section-content {
            padding: 25px;
        }

        .editable {
            background: var(--light-blue);
            border: 2px dashed var(--accent-blue);
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
        }

        .non-editable {
            background: #f9fafb;
            border: 1px solid var(--border);
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
        }

        .schedule-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }

        .schedule-table th, .schedule-table td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid var(--border);
        }

        .schedule-table th {
            background: var(--primary-blue);
            color: white;
            font-weight: 600;
        }

        .schedule-table tr:hover {
            background: var(--light-blue);
        }

        .objectives-list {
            list-style: none;
            padding: 0;
        }

        .objectives-list li {
            padding: 10px 0;
            border-bottom: 1px solid var(--border);
            position: relative;
            padding-left: 30px;
        }

        .objectives-list li:before {
            content: "✓";
            color: var(--success);
            font-weight: bold;
            position: absolute;
            left: 0;
            top: 10px;
        }

        .resources-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 15px;
        }

        .resource-card {
            background: var(--light-blue);
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid var(--primary-blue);
        }

        .resource-card h4 {
            color: var(--primary-blue);
            margin-bottom: 10px;
        }

        .save-btn {
            background: var(--success);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            margin-top: 10px;
            transition: background-color 0.3s;
        }

        .save-btn:hover {
            background: #059669;
        }

        .footer {
            text-align: center;
            padding: 30px;
            background: var(--primary-blue);
            color: white;
            border-radius: 10px;
            margin-top: 40px;
        }

        .assessment-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 15px;
        }

        .assessment-item {
            background: var(--light-blue);
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            border: 2px solid var(--accent-blue);
        }

        .assessment-item h4 {
            color: var(--primary-blue);
            margin-bottom: 10px;
        }

        .percentage {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--secondary-blue);
        }

        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }

            .header h1 {
                font-size: 2rem;
            }

            .instructor-info {
                grid-template-columns: 1fr;
            }

            .edit-btn {
                position: static;
                margin-top: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>IT120 - Network Essentials</h1>
            <p>CompTIA Network+ Certification Preparation</p>
            <p>North Seattle College | Business, Engineering & IT Division</p>
        </div>

        <!-- Title Bar Section -->
        <div class="title-bar">
            <h2>📋 Instructor Information</h2>
            <div class="instructor-info">
                <div class="info-group">
                    <label for="instructor-name">Instructor Name:</label>
                    <input type="text" id="instructor-name" value="Allan Kafley" />
                </div>
                <div class="info-group">
                    <label for="instructor-email">Email:</label>
                    <input type="email" id="instructor-email" value="allan.kafley@seattlecolleges.edu" />
                </div>
                <div class="info-group">
                    <label for="instructor-phone">Phone:</label>
                    <input type="tel" id="instructor-phone" value="(206) 372-9543" />
                </div>
                <div class="info-group">
                    <label for="office-hours">Office Hours:</label>
                    <input type="text" id="office-hours" value="Wed/Thurs 10:00 AM - 12:00 PM" />
                </div>
                <div class="info-group">
                    <label for="office-location">Office Location:</label>
                    <input type="text" id="office-location" value="Zoom Meeting" />
                </div>
                <div class="info-group">
                    <label for="department">Department:</label>
                    <input type="text" id="department" value="Information Technology" />
                </div>
            </div>
            <button class="save-btn" onclick="saveInstructorInfo()">💾 Save Instructor Information</button>
        </div>

        <!-- Course Information -->
        <div class="course-section">
            <div class="section-header">
                <h3>📚 Course Information</h3>
                <p>Basic course details and logistics</p>
                <button class="edit-btn" onclick="toggleEdit('course-info')">✏️ Edit</button>
            </div>
            <div class="section-content">
                <div id="course-info" class="editable">
                    <div class="info-group">
                        <label for="course-code">Course Code:</label>
                        <input type="text" id="course-code" value="IT 120" />
                    </div>
                    <div class="info-group">
                        <label for="course-title">Course Title:</label>
                        <input type="text" id="course-title" value="Network Essentials - Comptia Network +" />
                    </div>
                    <div class="info-group">
                        <label for="credits">Credits:</label>
                        <input type="text" id="credits" value="5" />
                    </div>
                    <div class="info-group">
                        <label for="quarter">Quarter:</label>
                        <input type="text" id="quarter" value="Fall 2025" />
                    </div>
                    <div class="info-group">
                        <label for="recquirement">Course Prerequisite(s):</label>
                        <input type="text" id="recquirement" value="EET 131 (See details below)" />
                    </div>
                    <div class="info-group">
                        <label for="meeting-time">Meeting Time:</label>
                        <input type="text" id="meeting-time" value="This asynchronous online course offers flexible learning with no set meeting times. Work at your own pace, but adhere to weekly deadlines. For personalized support, book a 1:1 Zoom meeting during office hours using the Calendly link." />
                    </div>
                    <div class="info-group">
                        <label for="location">Location:</label>
                        <input type="text" id="location" value="Online" />
                    </div>
                    <button class="save-btn" onclick="saveCourseInfo()">💾 Save Course Information</button>
                </div>
            </div>
        </div>

        <!-- Course Description -->
        <div class="course-section">
            <div class="section-header">
                <h3>📖 Course Description</h3>
                <p>Overview of course content and purpose</p>
                <button class="edit-btn" disabled>🔒 Non-Editable</button>
            </div>
            <div class="section-content">
                <div class="non-editable">
                    <p><strong>Catalog Course Description:</strong></p>
                    <p>Understand core protocols, devices, and technologies for wired and wireless networking. Intro to current networking technology for local area networks (LANs), wide area networks (WANs) and the Internet. Introduces key concepts and practices for network security, management, and troubleshooting.</p>
                    
                    <p><strong>Class Schedule Description:</strong></p>
                    <p>Provides the background and general introduction necessary to understand network technologies. Covers local and wide area networks and the Internet. Introduces routers, switches, firewalls, and network security. Prepares for Cisco, Windows, and Linux networking courses.</p>
                    
                    <p><strong>Prerequisites:</strong> EET 131 (may be taken concurrently) or permission. Note: A+ certification may be substituted for EET 131.</p>
                    
                    <p><strong>Program Requirement:</strong> This course is a requirement for the CISCO CRT NTWRK AS (527F) program and supports the expanded 20-credit Cisco Network Administration certificate program.</p>
                </div>
            </div>
        </div>

        <!-- Learning Objectives -->
        <div class="course-section">
            <div class="section-header">
                <h3>🎯 Learning Objectives</h3>
                <p>What students will achieve by the end of this course</p>
                <button class="edit-btn" disabled>🔒 Non-Editable</button>
            </div>
            <div class="section-content">
                <div class="non-editable">
                    <p><strong>Course Outcomes - Upon successful completion of this course, students will be able to:</strong></p>
                    <ul class="objectives-list">
                        <li>Identify basic networking elements, including cables, connectors, wired and wireless network devices</li>
                        <li>Configure networking devices to communicate over protocols such as Ethernet and IP</li>
                        <li>Distinguish between network devices such as switches, routers, and firewalls</li>
                        <li>Specify steps required for the design and deployment of wireless and wide area networks</li>
                        <li>Show the importance of policies and procedures for network management, security and optimization</li>
                        <li>Demonstrate knowledge and understanding of networking concepts consistent with the objectives of the CompTIA Network+ exam</li>
                    </ul>
                    
                    <p><strong>AA Degree Outcomes:</strong></p>
                    <ul class="objectives-list">
                        <li><strong>Technology Literacy:</strong> Effectively and critically evaluate, navigate, and use a range of digital technologies</li>
                        <li><strong>Critical thinking and problem solving:</strong> Complete labs that serve as individual problems to be solved, teaching how, when and why to connect network devices for data communication</li>
                        <li><strong>Technological proficiency:</strong> Configure network devices for data communications over the TCP/IP protocol stack</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Course Schedule -->
        <div class="course-section">
            <div class="section-header">
                <h3>📅 Course Schedule</h3>
                <p>Weekly topics and important dates</p>
                <button class="edit-btn" onclick="toggleEdit('schedule')">✏️ Edit</button>
            </div>
            <div class="section-content">
                <div id="schedule" class="editable">
                    <table class="schedule-table">
                        <thead>
                            <tr>
                                <th>Week</th>
                                <th>Date</th>
                                <th>Topic</th>
                                <th>Assignments Due</th>
                            </tr>
                        </thead>
                        <tbody id="schedule-body">
                            <tr>
                                <td>1</td>
                                <td>Week 1</td>
                                <td>Networking Basics</td>
                                <td>Course Introduction, Lab Setup</td>
                            </tr>
                            <tr>
                                <td>2</td>
                                <td>Week 2</td>
                                <td>Cables & Connectors</td>
                                <td>Lab 1: Cable Identification & Testing</td>
                            </tr>
                            <tr>
                                <td>3</td>
                                <td>Week 3</td>
                                <td>Networking Devices</td>
                                <td>Quiz 1: Networking Basics</td>
                            </tr>
                            <tr>
                                <td>4</td>
                                <td>Week 4</td>
                                <td>Ethernet Technology</td>
                                <td>Lab 2: Device Configuration</td>
                            </tr>
                            <tr>
                                <td>5</td>
                                <td>Week 5</td>
                                <td>IP Configuration</td>
                                <td>Lab 3: IP Addressing & Subnetting</td>
                            </tr>
                            <tr>
                                <td>6</td>
                                <td>Week 6</td>
                                <td>Switch Management</td>
                                <td>Quiz 2: Ethernet & IP</td>
                            </tr>
                            <tr>
                                <td>7</td>
                                <td>Week 7</td>
                                <td>Routing Fundamentals</td>
                                <td>Lab 4: Switch Configuration</td>
                            </tr>
                            <tr>
                                <td>8</td>
                                <td>Week 8</td>
                                <td>Firewalls & Security</td>
                                <td>Lab 5: Routing Configuration</td>
                            </tr>
                            <tr>
                                <td>9</td>
                                <td>Week 9</td>
                                <td>Network Customization & Wireless Networking</td>
                                <td>Quiz 3: Routing & Switching</td>
                            </tr>
                            <tr>
                                <td>10</td>
                                <td>Week 10</td>
                                <td>Wide Area Networking (WANs) & Network Policies</td>
                                <td>Lab 6: Wireless Configuration</td>
                            </tr>
                            <tr>
                                <td>11</td>
                                <td>Week 11</td>
                                <td>Network Security, Management & Optimization</td>
                                <td>Final Exam & Lab Practical</td>
                            </tr>
                        </tbody>
                    </table>
                    <button class="save-btn" onclick="saveSchedule()">💾 Save Schedule</button>
                </div>
            </div>
        </div>

        <!-- Assessment Methods -->
        <div class="course-section">
            <div class="section-header">
                <h3>📊 Assessment Methods</h3>
                <p>How student performance will be evaluated</p>
                <button class="edit-btn" disabled>🔒 Non-Editable</button>
            </div>
            <div class="section-content">
                <div class="non-editable">
                    <div class="assessment-grid">
                        <div class="assessment-item">
                            <h4>Quizzes</h4>
                            <div class="percentage">20%</div>
                            <p>Weekly concept checks</p>
                        </div>
                        <div class="assessment-item">
                            <h4>Lab Assignments</h4>
                            <div class="percentage">25%</div>
                            <p>Hands-on practical work</p>
                        </div>
                        <div class="assessment-item">
                            <h4>Midterm Exam</h4>
                            <div class="percentage">20%</div>
                            <p>Comprehensive mid-course exam</p>
                        </div>
                        <div class="assessment-item">
                            <h4>Final Project</h4>
                            <div class="percentage">15%</div>
                            <p>Network design project</p>
                        </div>
                        <div class="assessment-item">
                            <h4>Final Exam</h4>
                            <div class="percentage">20%</div>
                            <p>CompTIA Network+ practice exam</p>
                        </div>
                    </div>
                    <div style="margin-top: 20px;">
                        <h4>Grading Scale:</h4>
                        <p>A: 90-100% | B: 80-89% | C: 70-79% | D: 60-69% | F: Below 60%</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Required Resources -->
        <div class="course-section">
            <div class="section-header">
                <h3>📚 Required Resources</h3>
                <p>Textbooks, software, and materials needed</p>
                <button class="edit-btn" disabled>🔒 Non-Editable</button>
            </div>
            <div class="section-content">
                <div class="non-editable">
                    <div class="resources-grid">
                        <div class="resource-card">
                            <h4>📖 Textbook</h4>
                            <p><strong>CompTIA Network+ Study Guide</strong><br>
                            By Todd Lammle<br>
                            ISBN: 978-1119432258<br>
                            5th Edition</p>
                        </div>
                        <div class="resource-card">
                            <h4>🔧 Software</h4>
                            <p><strong>Packet Tracer</strong><br>
                            Cisco Network Simulator<br>
                            <strong>Wireshark</strong><br>
                            Network Protocol Analyzer</p>
                        </div>
                        <div class="resource-card">
                            <h4>💻 Hardware</h4>
                            <p><strong>Lab Equipment</strong><br>
                            Ethernet Cables<br>
                            Network Switches<br>
                            Wireless Access Points</p>
                        </div>
                        <div class="resource-card">
                            <h4>🌐 Online Resources</h4>
                            <p><strong>CompTIA Learning Platform</strong><br>
                            Professor Messer Videos<br>
                            NSC Canvas LMS<br>
                            Practice Exam Sites</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Course Policies -->
        <div class="course-section">
            <div class="section-header">
                <h3>📋 Course Policies</h3>
                <p>Important rules and expectations</p>
                <button class="edit-btn" disabled>🔒 Non-Editable</button>
            </div>
            <div class="section-content">
                <div class="non-editable">
                    <h4>Attendance Policy</h4>
                    <p>Regular attendance is essential for success. Students missing more than 2 classes may be dropped from the course. All absences must be reported to the instructor.</p>
                    
                    <h4>Late Assignment Policy</h4>
                    <p>Late assignments will be penalized 10% per day late. No assignments will be accepted more than one week after the due date without prior arrangement.</p>
                    
                    <h4>Academic Integrity</h4>
                    <p>All work must be original. Plagiarism or cheating will result in failure. Students may collaborate on lab assignments but must submit individual work.</p>
                    
                    <h4>Makeup Policy</h4>
                    <p>Makeup exams will only be given for documented emergencies. Students must contact the instructor within 24 hours of the missed exam.</p>
                    
                    <h4>Disability Support</h4>
                    <p>Students with disabilities should contact the Disability Support Services office to arrange appropriate accommodations.</p>
                </div>
            </div>
        </div>

        <div class="footer">
            <p>&copy; 2025 North Seattle College | Information Technology Department</p>
            <p>CompTIA Network+ Certification Preparation Course</p>
        </div>
    </div>

    <script>
        let editModes = {
            'course-info': false,
            'schedule': false
        };

        function toggleEdit(sectionId) {
            const section = document.getElementById(sectionId);
            const button = section.parentElement.querySelector('.edit-btn');
            
            if (editModes[sectionId]) {
                // Exit edit mode
                section.classList.remove('editable');
                section.classList.add('non-editable');
                button.innerHTML = '✏️ Edit';
                editModes[sectionId] = false;
            } else {
                // Enter edit mode
                section.classList.remove('non-editable');
                section.classList.add('editable');
                button.innerHTML = '💾 Save';
                editModes[sectionId] = true;
            }
        }

        function saveInstructorInfo() {
            const formData = {
                name: document.getElementById('instructor-name').value,
                email: document.getElementById('instructor-email').value,
                phone: document.getElementById('instructor-phone').value,
                officeHours: document.getElementById('office-hours').value,
                officeLocation: document.getElementById('office-location').value,
                department: document.getElementById('department').value
            };
            
            showNotification('Instructor information saved successfully!', 'success');
            console.log('Instructor Info Saved:', formData);
        }

        function saveCourseInfo() {
            const formData = {
                courseCode: document.getElementById('course-code').value,
                courseTitle: document.getElementById('course-title').value,
                credits: document.getElementById('credits').value,
                semester: document.getElementById('semester').value,
                section: document.getElementById('section').value,
                meetingTime: document.getElementById('meeting-time').value,
                location: document.getElementById('location').value
            };
            
            showNotification('Course information saved successfully!', 'success');
            console.log('Course Info Saved:', formData);
            
            // Exit edit mode
            toggleEdit('course-info');
        }

        function saveSchedule() {
            const scheduleRows = document.querySelectorAll('#schedule-body tr');
            const scheduleData = [];
            
            scheduleRows.forEach(row => {
                const cells = row.querySelectorAll('td');
                if (cells.length >= 4) {
                    scheduleData.push({
                        week: cells[0].textContent,
                        date: cells[1].textContent,
                        topic: cells[2].textContent,
                        assignments: cells[3].textContent
                    });
                }
            });
            
            showNotification('Schedule saved successfully!', 'success');
            console.log('Schedule Saved:', scheduleData);
            
            // Exit edit mode
            toggleEdit('schedule');
        }

        function showNotification(message, type) {
            const notification = document.createElement('div');
            notification.style.cssText = `
                position: fixed;
                top: 20px;
                right: 20px;
                padding: 15px 20px;
                border-radius: 5px;
                color: white;
                font-weight: bold;
                z-index: 1000;
                animation: slideIn 0.3s ease-out;
                background-color: ${type === 'success' ? 'var(--success)' : 'var(--warning)'};
            `;
            notification.textContent = message;
            
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.remove();
            }, 3000);
        }

        // Add CSS animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes slideIn {
                from {
                    transform: translateX(100%);
                    opacity: 0;
                }
                to {
                    transform: translateX(0);
                    opacity: 1;
                }
            }
        `;
        document.head.appendChild(style);

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            console.log('CompTIA Network+ Syllabus loaded successfully');
        });
    </script>
</body>
</html>
