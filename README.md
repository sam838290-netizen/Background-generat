<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مولد الخلفيات الذكية للمنتجات</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;900&family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1e40af;
            --secondary: #ec4899;
            --background: #f8fafc;
            --surface: #ffffff;
            --text: #1e293b;
            --text-secondary: #64748b;
            --border: #e2e8f0;
            --success: #10b981;
            --gradient-1: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            --gradient-2: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            --gradient-3: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        }

        .dark {
            --primary: #3b82f6;
            --primary-dark: #2563eb;
            --secondary: #f472b6;
            --background: #0f172a;
            --surface: #1e293b;
            --text: #f1f5f9;
            --text-secondary: #94a3b8;
            --border: #334155;
            --success: #34d399;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Tajawal', sans-serif;
            background: var(--background);
            color: var(--text);
            min-height: 100vh;
            transition: background 0.3s, color 0.3s;
        }

        h1, h2, h3 {
            font-family: 'Cairo', sans-serif;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1.5rem;
        }

        .header {
            background: var(--gradient-1);
            padding: 2.5rem 1.5rem;
            text-align: center;
            margin-bottom: 2rem;
            border-radius: 1rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .header h1 {
            color: white;
            font-size: 2.5rem;
            font-weight: 900;
            margin-bottom: 0.5rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .header p {
            color: rgba(255,255,255,0.95);
            font-size: 1.1rem;
            font-weight: 400;
        }

        .card {
            background: var(--surface);
            border-radius: 1rem;
            padding: 2rem;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            margin-bottom: 1.5rem;
            border: 1px solid var(--border);
            transition: all 0.3s;
        }

        .card:hover {
            box-shadow: 0 8px 30px rgba(0,0,0,0.12);
            transform: translateY(-2px);
        }

        .upload-area {
            border: 3px dashed var(--border);
            border-radius: 1rem;
            padding: 3rem 2rem;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            background: var(--background);
        }

        .upload-area:hover {
            border-color: var(--primary);
            background: var(--surface);
        }

        .upload-area.active {
            border-color: var(--primary);
            background: rgba(37, 99, 235, 0.05);
        }

        .upload-icon {
            font-size: 4rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .preview-container {
            margin-top: 1.5rem;
            text-align: center;
        }

        .preview-image {
            max-width: 100%;
            max-height: 500px;
            border-radius: 0.75rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
            object-fit: contain;
            background: var(--background);
            padding: 1rem;
        }

        .logo-preview {
            max-width: 150px;
            max-height: 150px;
            border-radius: 0.5rem;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            margin-top: 1rem;
            object-fit: contain;
            background: var(--background);
            padding: 0.5rem;
        }

        .input-group {
            margin-bottom: 1.5rem;
        }

        .input-group label {
            display: block;
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: var(--text);
            font-size: 1rem;
        }

        .input-group input,
        .input-group select,
        .input-group textarea {
            width: 100%;
            padding: 0.875rem 1rem;
            border: 2px solid var(--border);
            border-radius: 0.5rem;
            font-size: 1rem;
            font-family: 'Tajawal', sans-serif;
            background: var(--background);
            color: var(--text);
            transition: all 0.3s;
        }

        .input-group input:focus,
        .input-group select:focus,
        .input-group textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
        }

        .input-group textarea {
            resize: vertical;
            min-height: 100px;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 0.75rem;
            font-size: 1.1rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
            font-family: 'Cairo', sans-serif;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: var(--gradient-1);
            color: white;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(102, 126, 234, 0.5);
        }

        .btn-primary:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none;
        }

        .btn-secondary {
            background: var(--gradient-2);
            color: white;
            box-shadow: 0 4px 15px rgba(245, 87, 108, 0.4);
        }

        .btn-secondary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(245, 87, 108, 0.5);
        }

        .loading-spinner {
            display: inline-block;
            width: 1.2rem;
            height: 1.2rem;
            border: 3px solid rgba(255,255,255,0.3);
            border-top-color: white;
            border-radius: 50%;
            animation: spin 0.8s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        .result-section {
            display: none;
            margin-top: 2rem;
        }

        .result-section.active {
            display: block;
        }

        .result-image {
            max-width: 100%;
            border-radius: 1rem;
            box-shadow: 0 8px 30px rgba(0,0,0,0.15);
            margin-bottom: 1.5rem;
        }

        .download-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .download-card {
            background: var(--gradient-3);
            padding: 1.5rem;
            border-radius: 0.75rem;
            text-align: center;
            color: white;
            cursor: pointer;
            transition: all 0.3s;
        }

        .download-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
        }

        .download-card h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        .download-card p {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        .status-message {
            padding: 1rem 1.5rem;
            border-radius: 0.75rem;
            margin-bottom: 1.5rem;
            font-weight: 500;
            display: none;
        }

        .status-message.active {
            display: block;
        }

        .status-message.info {
            background: rgba(59, 130, 246, 0.1);
            color: var(--primary);
            border: 1px solid rgba(59, 130, 246, 0.3);
        }

        .status-message.error {
            background: rgba(239, 68, 68, 0.1);
            color: #dc2626;
            border: 1px solid rgba(239, 68, 68, 0.3);
        }

        .edit-title-section {
            background: var(--background);
            padding: 1.5rem;
            border-radius: 0.75rem;
            margin-bottom: 1.5rem;
            border: 2px solid var(--border);
        }

        .title-display {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 1rem;
            text-align: center;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 1.8rem;
            }

            .card {
                padding: 1.5rem;
            }

            .download-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Dark mode support */
        @media (prefers-color-scheme: dark) {
            .dark .upload-area {
                background: var(--background);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🎨 مولد الخلفيات الذكية للمنتجات</h1>
            <p>حوّل صور منتجاتك إلى إعلانات تسويقية احترافية تجذب العملاء وتزيد المبيعات</p>
        </div>

        <div id="statusMessage" class="status-message"></div>

        <div class="card">
            <h2 style="margin-bottom: 1.5rem; font-size: 1.8rem; color: var(--primary);">📸 تحميل صورة المنتج</h2>
            <p style="margin-bottom: 1rem; color: var(--text-secondary); font-size: 0.95rem;">
                ⭐ <strong>ملاحظة مهمة:</strong> سيتم تكبير المنتج ليملأ 60-70% من الصورة النهائية لضمان وضوحه التام وجذب انتباه العملاء
            </p>

            <div class="upload-area" id="uploadArea">
                <div class="upload-icon">📤</div>
                <h3 style="margin-bottom: 0.5rem; font-size: 1.3rem;">اضغط لتحميل صورة المنتج</h3>
                <p style="color: var(--text-secondary);">أو اسحب الصورة وأفلتها هنا</p>
                <input type="file" id="fileInput" accept="image/*" style="display: none;">
            </div>

            <div id="previewContainer" class="preview-container" style="display: none;">
                <img id="previewImage" class="preview-image" alt="معاينة المنتج">
            </div>
        </div>

        <div class="card">
            <h2 style="margin-bottom: 1.5rem; font-size: 1.8rem; color: var(--primary);">⚙️ خيارات التصميم</h2>

            <div class="input-group">
                <label for="productTitle">📝 عنوان المنتج (اختياري)</label>
                <input type="text" id="productTitle" placeholder='مثال: "اكتشف المستقبل الآن" أو "الأناقة تبدأ هنا" أو اتركه فارغاً'>
                <p style="font-size: 0.85rem; color: var(--text-secondary); margin-top: 0.5rem;">
                    💡 <strong>أمثلة للعناوين المثيرة:</strong><br>
                    • "اكتشف المستقبل الآن" 🚀<br>
                    • "الأناقة تبدأ هنا" ✨<br>
                    • "تجربة لا تُنسى" 🌟<br>
                    • "ارتقِ بأسلوبك" 👑<br>
                    • "الجودة تتحدث عن نفسها" 💎
                </p>
            </div>

            <div class="input-group">
                <label for="logoUpload">🎨 رفع الشعار (اختياري)</label>
                <input type="file" id="logoUpload" accept="image/*" style="padding: 0.75rem;">
                <p style="font-size: 0.85rem; color: var(--text-secondary); margin-top: 0.5rem;">سيتم وضع الشعار في الزاوية العلوية للصورة</p>
                <div id="logoPreviewContainer" style="display: none; text-align: center;">
                    <img id="logoPreview" class="logo-preview" alt="معاينة الشعار">
                </div>
            </div>

            <div class="input-group">
                <label for="aspectRatio">📐 نسبة الأبعاد</label>
                <select id="aspectRatio">
                    <option value="1:1">مربع (1:1) - إنستغرام</option>
                    <option value="16:9">أفقي (16:9) - مواقع ويب</option>
                    <option value="9:16">عمودي (9:16) - ستوريز</option>
                    <option value="4:3">قياسي (4:3)</option>
                    <option value="3:4">عمودي (3:4)</option>
                </select>
            </div>

            <button class="btn btn-primary" id="generateBtn" style="width: 100%; margin-top: 1rem;" disabled>
                <span id="btnText">✨ توليد الخلفية تلقائياً</span>
            </button>
        </div>

        <div id="resultSection" class="result-section card">
            <h2 style="margin-bottom: 1.5rem; font-size: 1.8rem; color: var(--success);">✨ النتيجة النهائية</h2>

            <div class="edit-title-section" id="editTitleSection">
                <div class="title-display" id="titleDisplay"></div>
                <div style="display: flex; gap: 0.75rem; align-items: flex-end;">
                    <div style="flex: 1;">
                        <label style="display: block; font-weight: 600; margin-bottom: 0.5rem; color: var(--text);">تعديل العنوان</label>
                        <input type="text" id="newTitle" style="width: 100%; padding: 0.875rem 1rem; border: 2px solid var(--border); border-radius: 0.5rem; font-size: 1rem; font-family: 'Tajawal', sans-serif; background: var(--surface); color: var(--text);">
                    </div>
                    <button class="btn btn-secondary" id="regenerateBtn" style="padding: 0.875rem 1.5rem;">
                        🔄 تطبيق التغيير
                    </button>
                </div>
            </div>

            <div style="text-align: center;">
                <img id="resultImage" class="result-image" alt="الصورة النهائية">
            </div>

            <h3 style="margin-top: 2rem; margin-bottom: 1rem; font-size: 1.5rem; color: var(--primary);">💾 تحميل بأحجام مختلفة</h3>

            <div class="download-grid">
                <div class="download-card" data-size="instagram">
                    <h3>📱 إنستغرام</h3>
                    <p>1080 × 1080 بكسل</p>
                </div>
                <div class="download-card" data-size="facebook">
                    <h3>📘 فيسبوك</h3>
                    <p>1200 × 630 بكسل</p>
                </div>
                <div class="download-card" data-size="twitter">
                    <h3>🐦 تويتر</h3>
                    <p>1200 × 675 بكسل</p>
                </div>
                <div class="download-card" data-size="story">
                    <h3>📲 ستوري</h3>
                    <p>1080 × 1920 بكسل</p>
                </div>
                <div class="download-card" data-size="website">
                    <h3>🌐 موقع ويب</h3>
                    <p>1920 × 1080 بكسل</p>
                </div>
                <div class="download-card" data-size="original">
                    <h3>🖼️ الأصلية</h3>
                    <p>الحجم الكامل</p>
                </div>
            </div>

            <button class="btn btn-secondary" id="createNewBtn" style="width: 100%; margin-top: 2rem;">
                ➕ إنشاء تصميم جديد
            </button>
        </div>
    </div>

    <script>
        // Dark mode detection
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            if (event.matches) {
                document.documentElement.classList.add('dark');
            } else {
                document.documentElement.classList.remove('dark');
            }
        });

        // Global variables
        let selectedFile = null;
        let logoFile = null;
        let generatedImageUrl = null;
        let currentTitle = '';

        // DOM elements
        const uploadArea = document.getElementById('uploadArea');
        const fileInput = document.getElementById('fileInput');
        const previewContainer = document.getElementById('previewContainer');
        const previewImage = document.getElementById('previewImage');
        const generateBtn = document.getElementById('generateBtn');
        const btnText = document.getElementById('btnText');
        const resultSection = document.getElementById('resultSection');
        const resultImage = document.getElementById('resultImage');
        const statusMessage = document.getElementById('statusMessage');
        const createNewBtn = document.getElementById('createNewBtn');
        const logoUpload = document.getElementById('logoUpload');
        const logoPreview = document.getElementById('logoPreview');
        const logoPreviewContainer = document.getElementById('logoPreviewContainer');
        const titleDisplay = document.getElementById('titleDisplay');
        const newTitleInput = document.getElementById('newTitle');
        const regenerateBtn = document.getElementById('regenerateBtn');

        // Upload area click
        uploadArea.addEventListener('click', () => fileInput.click());

        // File input change
        fileInput.addEventListener('change', (e) => {
            const file = e.target.files[0];
            if (file && file.type.startsWith('image/')) {
                handleFile(file);
            }
        });

        // Drag and drop
        uploadArea.addEventListener('dragover', (e) => {
            e.preventDefault();
            uploadArea.classList.add('active');
        });

        uploadArea.addEventListener('dragleave', () => {
            uploadArea.classList.remove('active');
        });

        uploadArea.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadArea.classList.remove('active');
            const file = e.dataTransfer.files[0];
            if (file && file.type.startsWith('image/')) {
                handleFile(file);
            }
        });

        // Handle file
        function handleFile(file) {
            selectedFile = file;
            const reader = new FileReader();
            reader.onload = (e) => {
                previewImage.src = e.target.result;
                previewContainer.style.display = 'block';
                generateBtn.disabled = false;
            };
            reader.readAsDataURL(file);
        }

        // Logo upload handler
        logoUpload.addEventListener('change', (e) => {
            const file = e.target.files[0];
            if (file && file.type.startsWith('image/')) {
                logoFile = file;
                const reader = new FileReader();
                reader.onload = (e) => {
                    logoPreview.src = e.target.result;
                    logoPreviewContainer.style.display = 'block';
                };
                reader.readAsDataURL(file);
            }
        });

        // Show status message
        function showStatus(message, type = 'info') {
            statusMessage.textContent = message;
            statusMessage.className = `status-message active ${type}`;
            statusMessage.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }

        // Hide status message
        function hideStatus() {
            statusMessage.className = 'status-message';
        }

        // Register Poe handler
        window.Poe.registerHandler('background-handler', async (result, context) => {
            const msg = result.responses[0];

            if (msg.status === 'error') {
                showStatus('حدث خطأ: ' + msg.statusText, 'error');
                generateBtn.disabled = false;
                regenerateBtn.disabled = false;
                btnText.innerHTML = '✨ توليد الخلفية تلقائياً';
            } else if (msg.status === 'incomplete') {
                // Keep showing loading state
            } else if (msg.status === 'complete') {
                if (msg.attachments && msg.attachments.length > 0) {
                    const imageAttachment = msg.attachments.find(att => att.isInline);
                    if (imageAttachment) {
                        generatedImageUrl = imageAttachment.url;

                        // If there's a logo, add it now
                        if (logoFile) {
                            showStatus('🎨 جاري إضافة الشعار...', 'info');
                            try {
                                // Create a canvas to combine image and logo
                                const img = new Image();
                                img.crossOrigin = 'anonymous';
                                img.onload = () => {
                                    const canvas = document.createElement('canvas');
                                    const ctx = canvas.getContext('2d');
                                    canvas.width = img.width;
                                    canvas.height = img.height;

                                    // Draw main image
                                    ctx.drawImage(img, 0, 0);

                                    // Draw logo
                                    const logo = new Image();
                                    logo.onload = () => {
                                        const logoSize = Math.min(img.width * 0.15, 150);
                                        const logoX = img.width - logoSize - 20;
                                        const logoY = 20;

                                        // Draw white background for logo
                                        ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
                                        ctx.fillRect(logoX - 10, logoY - 10, logoSize + 20, logoSize + 20);

                                        // Draw logo
                                        ctx.drawImage(logo, logoX, logoY, logoSize, logoSize);

                                        // Convert to URL
                                        generatedImageUrl = canvas.toDataURL('image/jpeg', 0.95);
                                        resultImage.src = generatedImageUrl;

                                        displayResult();
                                    };

                                    const reader = new FileReader();
                                    reader.onload = (e) => {
                                        logo.src = e.target.result;
                                    };
                                    reader.readAsDataURL(logoFile);
                                };
                                img.src = imageAttachment.url;
                            } catch (error) {
                                console.log('Error adding logo:', error);
                                resultImage.src = generatedImageUrl;
                                displayResult();
                            }
                        } else {
                            resultImage.src = generatedImageUrl;
                            displayResult();
                        }
                    } else {
                        showStatus('لم يتم توليد صورة. حاول مرة أخرى.', 'error');
                        generateBtn.disabled = false;
                        regenerateBtn.disabled = false;
                        btnText.innerHTML = '✨ توليد الخلفية تلقائياً';
                    }
                } else {
                    showStatus('لم يتم توليد صورة. حاول مرة أخرى.', 'error');
                    generateBtn.disabled = false;
                    regenerateBtn.disabled = false;
                    btnText.innerHTML = '✨ توليد الخلفية تلقائياً';
                }
            }
        });

        function displayResult() {
            // Extract and display title
            const userTitle = document.getElementById('productTitle').value.trim();
            const displayTitle = newTitleInput.value.trim() || userTitle || 'تم إنشاء عنوان تلقائياً على الصورة';
            currentTitle = displayTitle;
            titleDisplay.textContent = displayTitle;
            newTitleInput.value = displayTitle;

            resultSection.classList.add('active');
            resultSection.scrollIntoView({ behavior: 'smooth' });
            hideStatus();
            generateBtn.disabled = false;
            regenerateBtn.disabled = false;
            btnText.innerHTML = '✨ توليد الخلفية تلقائياً';
        }

        // Generate image function
        async function generateImage(customTitle = null) {
            if (!selectedFile) {
                showStatus('الرجاء تحميل صورة المنتج أولاً', 'error');
                return;
            }

            const aspectRatio = document.getElementById('aspectRatio').value;
            const userTitle = customTitle || document.getElementById('productTitle').value.trim();

            // Smart prompt - AI will analyze the product and create appropriate background
            let prompt = `Transform this product image into a stunning marketing advertisement:

CRITICAL REQUIREMENTS:
1. The product MUST be LARGE, PROMINENT, and take up 60-70% of the image - make it the hero
2. Product should be crystal clear, sharp, and perfectly lit
3. Add a sophisticated background that complements but never overshadows the product
4. Add 1-2 people in soft focus in the background representing target customers
5. People should be subtle and blurred, NOT competing with the product for attention
6. `;

            if (userTitle) {
                prompt += `Add this BOLD Arabic headline in large, eye-catching typography: "${userTitle}"
- Make the text large, bold, and impossible to miss
- Use premium, modern Arabic font
- Position it prominently but not covering the product`;
            } else {
                prompt += `Create a POWERFUL, EXCITING Arabic marketing headline that makes people want to buy
- Examples: "اكتشف المستقبل الآن" or "الأناقة تبدأ هنا" or "تجربة لا تُنسى"
- Make it SHORT (3-5 words), BOLD, and EMOTIONALLY compelling
- Use large, beautiful Arabic typography
- Make buyers feel they NEED this product`;
            }

            if (logoFile) {
                prompt += `\n7. Logo will be added separately in post-processing`;
                showStatus('ملاحظة: سيتم معالجة الشعار في خطوة منفصلة', 'info');
            }

            prompt += `

VISUAL HIERARCHY (most important first):
1. THE PRODUCT (biggest and clearest)
2. The Arabic headline (bold and attractive)
3. Background atmosphere
4. People (subtle, blurred, supporting role only)

Make this look like a premium advertisement that makes people stop scrolling and want to buy!`;

            // Disable button and show loading
            generateBtn.disabled = true;
            regenerateBtn.disabled = true;
            btnText.innerHTML = '<span class="loading-spinner"></span> جاري التحليل والتوليد...';
            showStatus('🤖 جاري تحليل المنتج وإنشاء إعلان احترافي مع خلفية ذكية وعنوان مثير... قد يستغرق هذا 30-60 ثانية', 'info');

            try {
                // Use GPT-Image-1 for better compatibility
                const botMessage = `@GPT-Image-1 ${prompt}`;
                const params = aspectRatio === '1:1' ? ' --aspect 1:1' : aspectRatio === '16:9' ? ' --aspect 3:2' : aspectRatio === '9:16' ? ' --aspect 2:3' : ' --aspect 1:1';

                await window.Poe.sendUserMessage(
                    botMessage + params,
                    {
                        handler: 'background-handler',
                        stream: false,
                        openChat: false,
                        attachments: [selectedFile]
                    }
                );
            } catch (error) {
                let errorMsg = 'حدث خطأ أثناء التوليد. حاول مرة أخرى.';

                if (error.errorType === 'USER_REJECTED_CONFIRMATION') {
                    errorMsg = 'تم إلغاء العملية. الرجاء الموافقة على طلب التحميل لاستخدام البوت.';
                } else if (error.errorType === 'INVALID_INPUT') {
                    errorMsg = 'خطأ في المدخلات. تأكد من صحة البيانات المدخلة.';
                } else if (error.message) {
                    errorMsg = 'خطأ: ' + error.message;
                }

                showStatus(errorMsg, 'error');
                generateBtn.disabled = false;
                regenerateBtn.disabled = false;
                btnText.innerHTML = '✨ توليد الخلفية تلقائياً';
                console.log('Error details:', error);
            }
        }

        // Generate button click
        generateBtn.addEventListener('click', () => generateImage());

        // Regenerate with new title
        regenerateBtn.addEventListener('click', () => {
            const newTitle = newTitleInput.value.trim();
            if (!newTitle) {
                showStatus('الرجاء إدخال عنوان جديد', 'error');
                return;
            }
            generateImage(newTitle);
        });

        // Download functionality
        document.querySelectorAll('.download-card').forEach(card => {
            card.addEventListener('click', async () => {
                if (!generatedImageUrl) return;

                const size = card.dataset.size;
                showStatus('جاري تحضير التحميل...', 'info');

                try {
                    // Fetch the image
                    const response = await fetch(generatedImageUrl);
                    const blob = await response.blob();

                    // Create canvas for resizing
                    const img = new Image();
                    img.crossOrigin = 'anonymous';

                    img.onload = () => {
                        const canvas = document.createElement('canvas');
                        const ctx = canvas.getContext('2d');

                        let width, height;
                        const sizes = {
                            'instagram': [1080, 1080],
                            'facebook': [1200, 630],
                            'twitter': [1200, 675],
                            'story': [1080, 1920],
                            'website': [1920, 1080],
                            'original': [img.width, img.height]
                        };

                        [width, height] = sizes[size] || sizes['original'];

                        canvas.width = width;
                        canvas.height = height;

                        // Draw image with proper scaling
                        const scale = Math.max(width / img.width, height / img.height);
                        const x = (width - img.width * scale) / 2;
                        const y = (height - img.height * scale) / 2;

                        ctx.fillStyle = '#ffffff';
                        ctx.fillRect(0, 0, width, height);
                        ctx.drawImage(img, x, y, img.width * scale, img.height * scale);

                        // Convert to blob and download
                        canvas.toBlob((blob) => {
                            const url = URL.createObjectURL(blob);
                            const a = document.createElement('a');
                            a.href = url;
                            a.download = `product-background-${size}.jpg`;
                            a.click();
                            URL.revokeObjectURL(url);
                            hideStatus();
                        }, 'image/jpeg', 0.95);
                    };

                    img.src = URL.createObjectURL(blob);
                } catch (error) {
                    showStatus('حدث خطأ أثناء التحميل. حاول مرة أخرى.', 'error');
                }
            });
        });

        // Create new design
        createNewBtn.addEventListener('click', () => {
            selectedFile = null;
            logoFile = null;
            generatedImageUrl = null;
            currentTitle = '';
            previewContainer.style.display = 'none';
            logoPreviewContainer.style.display = 'none';
            resultSection.classList.remove('active');
            fileInput.value = '';
            logoUpload.value = '';
            document.getElementById('productTitle').value = '';
            newTitleInput.value = '';
            titleDisplay.textContent = '';
            generateBtn.disabled = true;
            hideStatus();
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
    </script>
</body>
</html>

