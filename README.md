
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bioplasm NLS Pediatric & Children's Health Protocol Database</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #4c1d95 0%, #7c3aed 50%, #a855f7 100%);
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .category-respiratory { border-left: 4px solid #3b82f6; }
        .category-digestive { border-left: 4px solid #f59e0b; }
        .category-immune { border-left: 4px solid #10b981; }
        .category-developmental { border-left: 4px solid #8b5cf6; }
        .category-infectious { border-left: 4px solid #ef4444; }
        .category-endocrine { border-left: 4px solid #6366f1; }
        .category-skin { border-left: 4px solid #ec4899; }
        .category-musculoskeletal { border-left: 4px solid #059669; }
        .category-behavioral { border-left: 4px solid #9333ea; }
        .category-cardiovascular { border-left: 4px solid #dc2626; }
        .category-neurological { border-left: 4px solid #f97316; }
        .category-genetic { border-left: 4px solid #7c2d12; }
        .category-urogenital { border-left: 4px solid #0891b2; }
        .category-anxiety { border-left: 4px solid #f59e0b; }
        .category-mood { border-left: 4px solid #8b5cf6; }
        .category-sleep { border-left: 4px solid #6366f1; }
        .category-hematological { border-left: 4px solid #dc2626; }
        
        .frequency-badge {
            background: linear-gradient(45deg, #4f46e5, #7c3aed);
            color: white;
            padding: 2px 8px;
            border-radius: 12px;
            font-size: 0.75rem;
            font-weight: 500;
        }

        .severity-indicator {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            display: inline-block;
            margin-right: 8px;
        }

        .severity-mild { background-color: #22c55e; }
        .severity-moderate { background-color: #eab308; }
        .severity-severe { background-color: #ef4444; }

        .brain-icon {
            background: linear-gradient(45deg, #8b5cf6, #a855f7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header -->
    <header class="gradient-bg text-white shadow-lg">
        <div class="max-w-7xl mx-auto px-4 py-6">
            <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <div class="text-4xl mr-4">👶</div>
                    <div>
                        <h1 class="text-3xl font-bold">Pediatric & Children's Health Protocol Database</h1>
                        <p class="text-purple-100 mt-2">Specialized Bioplasm NLS Protocols for Children's Health Conditions & Development</p>
                        <p class="text-purple-200 mt-1 text-sm">Created by Anavrin Wellness</p>
                    </div>
                </div>
                <div class="text-right">
                    <div class="text-sm text-purple-100">Pediatric Edition</div>
                    <div class="text-sm text-purple-100">Updated: August 2025</div>
                </div>
            </div>
        </div>
    </header>

    <!-- Navigation & Search -->
    <div class="max-w-7xl mx-auto px-4 py-6">
        <div class="bg-white rounded-lg shadow-md p-6 mb-6">
            <div class="flex flex-col md:flex-row gap-4 items-center">
                <div class="flex-1">
                    <input type="text" id="searchInput" placeholder="Search pediatric protocols by condition, age group, or body system..." 
                           class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                </div>
                <div class="flex gap-3">
                    <select id="categoryFilter" class="px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500">
                        <option value="">All Categories</option>
                        <option value="respiratory">Respiratory Conditions</option>
                        <option value="digestive">Digestive & Nutritional</option>
                        <option value="immune">Immune & Allergic</option>
                        <option value="developmental">Developmental Disorders</option>
                        <option value="infectious">Infectious Diseases</option>
                        <option value="endocrine">Endocrine & Growth</option>
                        <option value="skin">Skin & Dermatological</option>
                        <option value="musculoskeletal">Musculoskeletal</option>
                        <option value="behavioral">Behavioral & Learning</option>
                        <option value="cardiovascular">Cardiovascular</option>
                        <option value="neurological">Neurological</option>
                        <option value="genetic">Genetic Conditions</option>
                        <option value="urogenital">Urogenital</option>
                        <option value="anxiety">Anxiety Disorders</option>
                        <option value="mood">Mood Disorders</option>
                        <option value="sleep">Sleep Disorders</option>
                        <option value="hematological">Blood Disorders</option>
                    </select>
                    <select id="severityFilter" class="px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500">
                        <option value="">All Severities</option>
                        <option value="mild">Mild</option>
                        <option value="moderate">Moderate</option>
                        <option value="severe">Severe</option>
                    </select>
                </div>
            </div>
        </div>

        <!-- Statistics Dashboard -->
        <div class="grid grid-cols-1 md:grid-cols-4 gap-6 mb-8">
            <div class="bg-white rounded-lg shadow-md p-6">
                <div class="flex items-center">
                    <div class="p-3 rounded-full bg-purple-100 text-purple-600">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path>
                        </svg>
                    </div>
                    <div class="ml-4">
                        <p class="text-sm font-medium text-gray-600">Pediatric Protocols</p>
                        <p class="text-2xl font-semibold text-gray-900" id="totalProtocols">73</p>
                    </div>
                </div>
            </div>
            
            <div class="bg-white rounded-lg shadow-md p-6">
                <div class="flex items-center">
                    <div class="p-3 rounded-full bg-blue-100 text-blue-600">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"></path>
                        </svg>
                    </div>
                    <div class="ml-4">
                        <p class="text-sm font-medium text-gray-600">Health Categories</p>
                        <p class="text-2xl font-semibold text-gray-900">13</p>
                    </div>
                </div>
            </div>
            
            <div class="bg-white rounded-lg shadow-md p-6">
                <div class="flex items-center">
                    <div class="p-3 rounded-full bg-green-100 text-green-600">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                        </svg>
                    </div>
                    <div class="ml-4">
                        <p class="text-sm font-medium text-gray-600">Healing Frequencies</p>
                        <p class="text-2xl font-semibold text-gray-900">447</p>
                    </div>
                </div>
            </div>
            
            <div class="bg-white rounded-lg shadow-md p-6">
                <div class="flex items-center">
                    <div class="p-3 rounded-full bg-orange-100 text-orange-600">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                        </svg>
                    </div>
                    <div class="ml-4">
                        <p class="text-sm font-medium text-gray-600">Avg Session</p>
                        <p class="text-2xl font-semibold text-gray-900">23min</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Energetic Body Mapping Section -->
        <div class="bg-white rounded-lg shadow-md p-6 mb-8">
            <div class="flex items-center justify-between mb-6">
                <h2 class="text-2xl font-bold text-gray-900">🔮 Pediatric Body Systems & Development Mapping</h2>
                <button id="toggleMapping" class="px-4 py-2 bg-purple-600 text-white rounded-lg hover:bg-purple-700 transition-colors">
                    Show Mapping Guide
                </button>
            </div>
            
            <div id="mappingContent" class="hidden">
                <p class="text-gray-600 mb-6">Understanding pediatric body systems and developmental stages for age-appropriate NLS scanning and treatment protocols.</p>
                
                <!-- Pediatric NLS Database Mapping Table -->
                <div class="mb-6">
                    <h3 class="text-xl font-bold text-purple-800 mb-4">📊 Pediatric NLS Database Mapping Table</h3>
                    <div class="overflow-x-auto">
                        <table class="w-full text-sm border-collapse border border-purple-300">
                            <thead>
                                <tr class="bg-purple-100">
                                    <th class="border border-purple-300 px-3 py-2 text-left font-semibold text-purple-800">Condition</th>
                                    <th class="border border-purple-300 px-3 py-2 text-left font-semibold text-purple-800">Primary Body System(s)</th>
                                    <th class="border border-purple-300 px-3 py-2 text-left font-semibold text-purple-800">Scan Area / NLS Focus Points</th>
                                    <th class="border border-purple-300 px-3 py-2 text-left font-semibold text-purple-800">Etalons to Test</th>
                                </tr>
                            </thead>
                            <tbody class="text-gray-700">
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Recurrent Ear Infections (Otitis Media)</td>
                                    <td class="border border-purple-300 px-3 py-2">Ear / Auditory System / Immune System</td>
                                    <td class="border border-purple-300 px-3 py-2">Middle ear, Eustachian tube, cochlea, auditory nerve pathways</td>
                                    <td class="border border-purple-300 px-3 py-2">Lymphoid tissue activity (adenoids, tonsils), T/B cells, IgA, cytokines</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Tonsillitis & Adenoiditis</td>
                                    <td class="border border-purple-300 px-3 py-2">Throat / Lymphatic / Immune System</td>
                                    <td class="border border-purple-300 px-3 py-2">Tonsils, adenoids, pharyngeal wall</td>
                                    <td class="border border-purple-300 px-3 py-2">Lymphoid tissue, MALT, T/B cell activity, cytokine profile</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Childhood Asthma</td>
                                    <td class="border border-purple-300 px-3 py-2">Respiratory System / Immune System</td>
                                    <td class="border border-purple-300 px-3 py-2">Bronchi, bronchioles, alveoli, upper airway mucosa</td>
                                    <td class="border border-purple-300 px-3 py-2">IgE/IgA response, cytokines (IL-4, IL-5, IL-13), lung parenchyma</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Allergic Rhinitis (Hay Fever)</td>
                                    <td class="border border-purple-300 px-3 py-2">Respiratory / Immune System</td>
                                    <td class="border border-purple-300 px-3 py-2">Nasal mucosa, sinuses, bronchi (if reactive)</td>
                                    <td class="border border-purple-300 px-3 py-2">IgE, histamine, eosinophil activity</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Eczema (Atopic Dermatitis)</td>
                                    <td class="border border-purple-300 px-3 py-2">Skin / Immune System</td>
                                    <td class="border border-purple-300 px-3 py-2">Epidermis, dermis, sebaceous and sweat glands</td>
                                    <td class="border border-purple-300 px-3 py-2">Langerhans cells, cytokines (IL-2, IL-6, TNF-α), histamine markers</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Juvenile Rheumatoid Arthritis</td>
                                    <td class="border border-purple-300 px-3 py-2">Musculoskeletal / Immune System</td>
                                    <td class="border border-purple-300 px-3 py-2">Synovial joints, cartilage, bones, skeletal muscles</td>
                                    <td class="border border-purple-300 px-3 py-2">ANA/RF, cytokines (IL-1, IL-6, TNF-α), inflammatory markers</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Kawasaki Disease</td>
                                    <td class="border border-purple-300 px-3 py-2">Cardiovascular / Immune System / Skin / Mucous Membranes</td>
                                    <td class="border border-purple-300 px-3 py-2">Heart (coronary arteries, valves), peripheral arteries/veins, skin, oral and conjunctival mucosa, lymph nodes</td>
                                    <td class="border border-purple-300 px-3 py-2">CRP, ESR, cytokines, vascular tone, neural reflex markers, immune cell activity</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Autism Spectrum Disorder (ASD)</td>
                                    <td class="border border-purple-300 px-3 py-2">Nervous System / Brain</td>
                                    <td class="border border-purple-300 px-3 py-2">Cerebral cortex, limbic system, cerebellum</td>
                                    <td class="border border-purple-300 px-3 py-2">Neurotransmitters (dopamine, serotonin, GABA), glial cell function, neural connectivity markers</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Attention-Deficit/Hyperactivity Disorder (ADHD)</td>
                                    <td class="border border-purple-300 px-3 py-2">Nervous System / Brain</td>
                                    <td class="border border-purple-300 px-3 py-2">Prefrontal cortex, basal ganglia</td>
                                    <td class="border border-purple-300 px-3 py-2">Dopamine/serotonin balance, neurotransmitter function, neural pathway efficiency</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Epilepsy / Childhood Seizure Disorders</td>
                                    <td class="border border-purple-300 px-3 py-2">Nervous System / Brain</td>
                                    <td class="border border-purple-300 px-3 py-2">Cerebral cortex, hippocampus</td>
                                    <td class="border border-purple-300 px-3 py-2">GABA/glutamate balance, ion channel function, neural excitability markers</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Developmental Delay</td>
                                    <td class="border border-purple-300 px-3 py-2">Nervous System / Multiple Systems</td>
                                    <td class="border border-purple-300 px-3 py-2">Brain regions (cortex, cerebellum), musculoskeletal system</td>
                                    <td class="border border-purple-300 px-3 py-2">Neurotransmitter markers, metabolic/endocrine profile, muscle function</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Cerebral Palsy</td>
                                    <td class="border border-purple-300 px-3 py-2">Nervous System / Musculoskeletal System</td>
                                    <td class="border border-purple-300 px-3 py-2">Motor cortex, basal ganglia, cerebellum, skeletal muscles</td>
                                    <td class="border border-purple-300 px-3 py-2">Neural reflex pathways, muscle tone, bone/joint health, neuromuscular junction function</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Pediatric Food Allergies</td>
                                    <td class="border border-purple-300 px-3 py-2">Digestive System / Immune System</td>
                                    <td class="border border-purple-300 px-3 py-2">Stomach, small intestine, gut-associated lymphoid tissue</td>
                                    <td class="border border-purple-300 px-3 py-2">IgE/IgA, cytokines, gut mucosa integrity</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Celiac Disease</td>
                                    <td class="border border-purple-300 px-3 py-2">Digestive System / Immune System</td>
                                    <td class="border border-purple-300 px-3 py-2">Small intestine villi, gut-associated lymphoid tissue</td>
                                    <td class="border border-purple-300 px-3 py-2">IgA antibodies (anti-tTG, anti-gliadin), cytokines, villi morphology</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Lactose Intolerance</td>
                                    <td class="border border-purple-300 px-3 py-2">Digestive System</td>
                                    <td class="border border-purple-300 px-3 py-2">Small intestine mucosa, lactase enzyme activity</td>
                                    <td class="border border-purple-300 px-3 py-2">Digestive enzyme levels, microbiome markers</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Infant Colic</td>
                                    <td class="border border-purple-300 px-3 py-2">Digestive System / Nervous System</td>
                                    <td class="border border-purple-300 px-3 py-2">Stomach, intestines</td>
                                    <td class="border border-purple-300 px-3 py-2">Gut motility, microbiome, inflammatory markers, neurotransmitter activity</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Reflux (GERD in children)</td>
                                    <td class="border border-purple-300 px-3 py-2">Digestive System / Esophagus / Stomach</td>
                                    <td class="border border-purple-300 px-3 py-2">Esophagus, lower esophageal sphincter, stomach lining</td>
                                    <td class="border border-purple-300 px-3 py-2">pH balance, gastric enzymes, mucosal integrity</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Frequent Colds & Viral Infections</td>
                                    <td class="border border-purple-300 px-3 py-2">Respiratory / Immune System</td>
                                    <td class="border border-purple-300 px-3 py-2">Nasal mucosa, pharynx, bronchi, lymphoid tissue</td>
                                    <td class="border border-purple-300 px-3 py-2">T/B/NK cell activity, IgA/IgG, interferon response</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Pediatric Migraines</td>
                                    <td class="border border-purple-300 px-3 py-2">Nervous System / Brain</td>
                                    <td class="border border-purple-300 px-3 py-2">Cerebral cortex, vascular system in brain</td>
                                    <td class="border border-purple-300 px-3 py-2">Neurotransmitters (serotonin, dopamine), pain pathway markers</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Sleep Disorders (night terrors, bedwetting, insomnia)</td>
                                    <td class="border border-purple-300 px-3 py-2">Nervous System / Brain / Urinary System</td>
                                    <td class="border border-purple-300 px-3 py-2">Brainstem, hypothalamus, pineal gland, kidneys/bladder</td>
                                    <td class="border border-purple-300 px-3 py-2">Neurotransmitters, melatonin, kidney/bladder function, hormonal balance</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Childhood Obesity</td>
                                    <td class="border border-purple-300 px-3 py-2">Endocrine / Metabolic / Musculoskeletal System</td>
                                    <td class="border border-purple-300 px-3 py-2">Adipose tissue, pancreas, liver, skeletal muscles</td>
                                    <td class="border border-purple-300 px-3 py-2">Insulin, leptin, ghrelin, lipid metabolism markers, musculoskeletal integrity</td>
                                </tr>
                                <tr class="hover:bg-purple-50">
                                    <td class="border border-purple-300 px-3 py-2 font-medium">Anemia (Iron Deficiency)</td>
                                    <td class="border border-purple-300 px-3 py-2">Blood / Hematologic System</td>
                                    <td class="border border-purple-300 px-3 py-2">Bone marrow, RBC production sites, duodenum</td>
                                    <td class="border border-purple-300 px-3 py-2">Hemoglobin, ferritin, transferrin, RBC count, nutrient absorption markers</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="space-y-6">
                        <div class="border border-purple-200 rounded-lg p-4">
                            <h3 class="text-lg font-semibold text-purple-800 mb-3">👶 1. Infancy & Early Development (0-2 years)</h3>
                            <div class="text-sm text-gray-700 mb-3">
                                <strong>Key Systems:</strong>
                                <ul class="list-disc list-inside mt-2 space-y-1">
                                    <li>Respiratory system (breathing patterns, lung development)</li>
                                    <li>Digestive system (feeding, colic, reflux)</li>
                                    <li>Immune system (maternal antibodies, vaccination response)</li>
                                    <li>Nervous system (reflexes, motor development)</li>
                                </ul>
                            </div>
                            <div class="text-xs text-purple-600 bg-purple-50 p-2 rounded">
                                <strong>Focus:</strong> Basic physiological functions, growth patterns, and foundational immune development.
                            </div>
                        </div>

                        <div class="border border-blue-200 rounded-lg p-4">
                            <h3 class="text-lg font-semibold text-blue-800 mb-3">🧒 2. Toddler Development (2-5 years)</h3>
                            <div class="text-sm text-gray-700 mb-3">
                                <strong>Key Systems:</strong>
                                <ul class="list-disc list-inside mt-2 space-y-1">
                                    <li>Motor coordination (gross and fine motor skills)</li>
                                    <li>Language development (speech, comprehension)</li>
                                    <li>Social-emotional regulation (tantrums, attachment)</li>
                                    <li>Sensory processing (sight, sound, touch integration)</li>
                                </ul>
                            </div>
                            <div class="text-xs text-blue-600 bg-blue-50 p-2 rounded">
                                <strong>Focus:</strong> Developmental milestones, behavioral regulation, and sensory integration.
                            </div>
                        </div>

                        <div class="border border-red-200 rounded-lg p-4">
                            <h3 class="text-lg font-semibold text-red-800 mb-3">🎒 3. School Age (6-12 years)</h3>
                            <div class="text-sm text-gray-700 mb-3">
                                <strong>Key Systems:</strong>
                                <ul class="list-disc list-inside mt-2 space-y-1">
                                    <li>Cognitive function (attention, learning, memory)</li>
                                    <li>Musculoskeletal system (growth spurts, coordination)</li>
                                    <li>Endocrine system (early hormonal changes)</li>
                                    <li>Cardiovascular fitness (activity tolerance)</li>
                                </ul>
                            </div>
                            <div class="text-xs text-red-600 bg-red-50 p-2 rounded">
                                <strong>Focus:</strong> Learning capacity, physical development, and social adaptation.
                            </div>
                        </div>
                    </div>

                    <div class="space-y-6">
                        <div class="border border-green-200 rounded-lg p-4">
                            <h3 class="text-lg font-semibold text-green-800 mb-3">🌱 4. Adolescent Transition (13-18 years)</h3>
                            <div class="text-sm text-gray-700 mb-3">
                                <strong>Key Systems:</strong>
                                <ul class="list-disc list-inside mt-2 space-y-1">
                                    <li>Hormonal system (puberty, growth hormones)</li>
                                    <li>Reproductive system (sexual development)</li>
                                    <li>Emotional regulation (mood swings, identity formation)</li>
                                    <li>Skin health (acne, hormonal changes)</li>
                                </ul>
                            </div>
                            <div class="text-xs text-green-600 bg-green-50 p-2 rounded">
                                <strong>Focus:</strong> Hormonal balance, emotional stability, and physical maturation.
                            </div>
                        </div>

                        <div class="border border-orange-200 rounded-lg p-4">
                            <h3 class="text-lg font-semibold text-orange-800 mb-3">🏥 5. Common Pediatric Conditions</h3>
                            <div class="text-sm text-gray-700 mb-3">
                                <strong>Frequent Issues:</strong>
                                <ul class="list-disc list-inside mt-2 space-y-1">
                                    <li>Allergies and asthma (respiratory hypersensitivity)</li>
                                    <li>Digestive issues (constipation, food sensitivities)</li>
                                    <li>Sleep disorders (night terrors, insomnia)</li>
                                    <li>Behavioral challenges (ADHD, autism spectrum)</li>
                                </ul>
                            </div>
                            <div class="text-xs text-orange-600 bg-orange-50 p-2 rounded">
                                <strong>Focus:</strong> Age-specific health challenges and developmental variations.
                            </div>
                        </div>

                        <div class="border border-indigo-200 rounded-lg p-4">
                            <h3 class="text-lg font-semibold text-indigo-800 mb-3">🧬 6. Genetic & Congenital Factors</h3>
                            <div class="text-sm text-gray-700 mb-3">
                                <strong>Considerations:</strong>
                                <ul class="list-disc list-inside mt-2 space-y-1">
                                    <li>Inherited conditions (metabolic disorders, genetic syndromes)</li>
                                    <li>Congenital anomalies (heart defects, neural tube defects)</li>
                                    <li>Family history patterns (allergies, autoimmune conditions)</li>
                                    <li>Epigenetic factors (environmental influences on gene expression)</li>
                                </ul>
                            </div>
                            <div class="text-xs text-indigo-600 bg-indigo-50 p-2 rounded">
                                <strong>Focus:</strong> Genetic predispositions, family patterns, and inherited health risks.
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Quick Reference Summary Table -->
                <div class="mt-6 p-4 bg-gradient-to-r from-purple-50 to-blue-50 rounded-lg border border-purple-200">
                    <h4 class="font-semibold text-purple-800 mb-4">📋 Pediatric Age Groups & Key Focus Areas</h4>
                    <div class="overflow-x-auto">
                        <table class="w-full text-sm">
                            <thead>
                                <tr class="border-b border-purple-200">
                                    <th class="text-left py-2 px-3 font-semibold text-purple-800">Age Group</th>
                                    <th class="text-left py-2 px-3 font-semibold text-purple-800">Primary Health Focus</th>
                                </tr>
                            </thead>
                            <tbody class="text-gray-700">
                                <tr class="border-b border-purple-100">
                                    <td class="py-2 px-3 font-medium">Infancy (0-2 years)</td>
                                    <td class="py-2 px-3">Respiratory, digestive, immune, nervous system development</td>
                                </tr>
                                <tr class="border-b border-purple-100">
                                    <td class="py-2 px-3 font-medium">Toddler (2-5 years)</td>
                                    <td class="py-2 px-3">Motor coordination, language, emotional regulation, sensory processing</td>
                                </tr>
                                <tr class="border-b border-purple-100">
                                    <td class="py-2 px-3 font-medium">School Age (6-12 years)</td>
                                    <td class="py-2 px-3">Cognitive function, musculoskeletal, endocrine, cardiovascular</td>
                                </tr>
                                <tr class="border-b border-purple-100">
                                    <td class="py-2 px-3 font-medium">Adolescent (13-18 years)</td>
                                    <td class="py-2 px-3">Hormonal system, reproductive development, emotional stability</td>
                                </tr>
                                <tr class="border-b border-purple-100">
                                    <td class="py-2 px-3 font-medium">Common Conditions</td>
                                    <td class="py-2 px-3">Allergies, asthma, digestive issues, sleep disorders, behavioral challenges</td>
                                </tr>
                                <tr>
                                    <td class="py-2 px-3 font-medium">Genetic Factors</td>
                                    <td class="py-2 px-3">Inherited conditions, congenital anomalies, family patterns</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>

                <div class="mt-4 pt-4 border-t border-purple-200">
                    <h5 class="font-semibold text-purple-800 mb-2">🔍 Pediatric Scanning Guidance for Practitioners:</h5>
                    <p class="text-sm text-gray-700">
                        Use age-appropriate protocols and consider developmental stages during NLS analysis. Always use gentler intensities for children, obtain parental consent, and coordinate with pediatric healthcare providers. Monitor for age-specific responses and adjust treatment duration accordingly.
                    </p>
                </div>
            </div>
        </div>

        <!-- Protocol Cards Grid -->
        <div id="protocolGrid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Protocol cards will be dynamically generated here -->
        </div>

        <!-- Protocol Detail Modal -->
        <div id="protocolModal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50">
            <div class="flex items-center justify-center min-h-screen p-4">
                <div class="bg-white rounded-lg shadow-xl max-w-6xl w-full max-h-screen overflow-y-auto">
                    <div class="p-6 border-b border-gray-200">
                        <div class="flex justify-between items-start">
                            <div>
                                <h2 id="modalTitle" class="text-2xl font-bold text-gray-900"></h2>
                                <p id="modalCategory" class="text-sm text-gray-600 mt-1"></p>
                                <div id="modalDSM" class="text-xs text-purple-600 mt-1 font-medium"></div>
                            </div>
                            <button onclick="closeModal()" class="text-gray-400 hover:text-gray-600">
                                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                                </svg>
                            </button>
                        </div>
                    </div>
                    
                    <div class="p-6" id="modalContent">
                        <!-- Content will be dynamically populated -->
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Comprehensive pediatric conditions database with updated body system mappings
        const protocols = [
            // Infectious & Immune Conditions
            {
                id: 1,
                name: "Recurrent Ear Infections (Otitis Media)",
                category: "infectious",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "6 months - 12 years",
                primarySystems: "Ear / Auditory System / Immune System",
                regions: ["Middle Ear Structures (Ossicles, Tympanic Membrane)", "Eustachian Tube", "Cochlea", "Auditory Nerve Pathways", "Lymphoid Tissue (Adenoids, Tonsils)"],
                neurotransmitters: ["T/B Cells", "B-Lymphocytes System", "IgA", "Middle Ear Function", "Auditory Processing", "Immune Response"],
                dsm: "ICD-10: H66.9",
                description: "Gentle protocol targeting recurrent middle ear infections through immune enhancement and Eustachian tube function optimization in children.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Use gentle intensity for children. Monitor for hearing changes. Coordinate with pediatric ENT. May reduce infection frequency. Position child comfortably during treatment."
            },
            {
                id: 2,
                name: "Tonsillitis & Adenoiditis",
                category: "infectious",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "2-12 years",
                primarySystems: "Throat / Lymphatic / Immune System",
                regions: ["Tonsils", "Adenoids", "Pharyngeal Lymph Nodes", "Salivary Glands", "MALT (Mucosa-Associated Lymphoid Tissue)"],
                neurotransmitters: ["T/B Cells", "T-Lymphocytes System", "Cytokine Profile", "IL-1 System", "Lymphatic Function", "Immune Response"],
                dsm: "ICD-10: J03.9",
                description: "Gentle protocol addressing chronic tonsil and adenoid inflammation through immune modulation and lymphatic drainage enhancement in children.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Use child-friendly positioning. Monitor for swallowing difficulties. May reduce surgical need. Coordinate with pediatric ENT. Support with probiotics."
            },
            {
                id: 3,
                name: "Childhood Asthma",
                category: "respiratory",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "2-18 years",
                primarySystems: "Respiratory System / Immune System",
                regions: ["Bronchi/Bronchioles", "Alveoli", "Diaphragm", "Mucous Membranes of Upper Airways", "Respiratory Muscles"],
                neurotransmitters: ["IgE/IgA Response", "B-Lymphocytes System", "T-Lymphocytes System", "Cytokine Profile (IL-4, IL-5, IL-13)", "IL-8 System", "Histamine"],
                dsm: "ICD-10: J45.9",
                description: "Child-safe protocol targeting bronchial hyperresponsiveness and allergic inflammation through gentle immune modulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Keep rescue inhaler available. Monitor breathing patterns. Use gentle intensity. May reduce attack frequency. Coordinate with pediatric pulmonologist."
            },
            {
                id: 4,
                name: "Allergic Rhinitis (Hay Fever)",
                category: "immune",
                severity: "mild",
                duration: "20 minutes",
                ageGroup: "3-18 years",
                primarySystems: "Respiratory / Immune System",
                regions: ["Nasal Mucosa", "Sinuses", "Bronchi (if reactive)", "Upper Respiratory Tract", "Lymphoid Tissue"],
                neurotransmitters: ["IgE", "B-Lymphocytes System", "IgG/IgA/IgM Levels", "Histamine Markers", "IL-8 System", "Mast Cell Mediators"],
                dsm: "ICD-10: J30.9",
                description: "Gentle protocol targeting allergic nasal inflammation and histamine response in children through immune system modulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Most effective during allergy season. May reduce need for antihistamines. Monitor for congestion changes. Combine with environmental controls."
            },
            {
                id: 5,
                name: "Eczema (Atopic Dermatitis)",
                category: "skin",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "3 months - 18 years",
                primarySystems: "Skin / Immune System",
                regions: ["Epidermis & Dermis", "Sebaceous/Sweat Glands", "Langerhans Cells", "Skin Barrier Function", "Hair Follicles"],
                neurotransmitters: ["Cytokine Profile (IL-2, IL-6, TNF-α)", "T-Lymphocytes System", "B-Lymphocytes System", "IL-1 System", "Histamine/Allergic Markers", "IgE"],
                dsm: "ICD-10: L20.9",
                description: "Gentle protocol addressing skin barrier dysfunction and allergic inflammation in children through immune modulation and skin repair.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor skin condition changes. May reduce itching and inflammation. Coordinate with pediatric dermatologist. Support with gentle skincare routine."
            },
            {
                id: 6,
                name: "Juvenile Rheumatoid Arthritis (JIA)",
                category: "musculoskeletal",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "1-16 years",
                primarySystems: "Musculoskeletal / Immune System",
                regions: ["Synovial Joints", "Cartilage", "Bones", "Skeletal Muscles", "Joint Capsules"],
                neurotransmitters: ["ANA/RF", "T-Lymphocytes System", "Cytokine Profile (IL-2, IL-6, TNF-α)", "IL-1 System", "CRP System", "C-reactive Protein Levels"],
                dsm: "ICD-10: M08.9",
                description: "Careful protocol targeting autoimmune joint inflammation in children through gentle immune modulation and tissue support.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor joint mobility and pain. Coordinate with pediatric rheumatologist. May reduce inflammation markers. Support with gentle exercise and physical therapy."
            },
            {
                id: 7,
                name: "Kawasaki Disease",
                category: "cardiovascular",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "6 months - 5 years",
                primarySystems: "Cardiovascular / Immune System / Skin / Mucous Membranes",
                regions: ["Coronary Arteries", "Heart Valves", "Peripheral Arteries/Veins", "Skin Rash Markers", "Oral/Conjunctival Mucosa", "Lymph Nodes"],
                neurotransmitters: ["CRP System", "C-reactive Protein Levels", "IL-1 System", "IL-8 System", "T-Lymphocytes System", "Inflammatory Markers"],
                dsm: "ICD-10: M30.3",
                description: "Emergency supportive protocol for systemic vasculitis in young children, targeting cardiac protection and inflammation reduction.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES IMMEDIATE MEDICAL SUPERVISION. Monitor cardiac function closely. Coordinate with pediatric cardiology. Support alongside IVIG treatment only."
            },

            // Neurological & Developmental Conditions
            {
                id: 8,
                name: "Autism Spectrum Disorder (ASD)",
                category: "developmental",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "18 months - 18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Cerebral Cortex", "Limbic System", "Neural Connectivity Centers", "Language Processing Areas", "Social Brain Networks"],
                neurotransmitters: ["Neurotransmitter Balance (Dopamine, Serotonin, GABA)", "Glial Cell Function", "Neural Connectivity Markers", "Oxytocin", "Glutamate"],
                dsm: "DSM-5: 299.00",
                description: "Very gentle protocol supporting social communication, reducing sensory sensitivities, and promoting neural connectivity in children with ASD.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Use VERY gentle intensities. Monitor for sensory responses. May improve social engagement. Coordinate with behavioral therapy. Allow breaks as needed."
            },
            {
                id: 9,
                name: "ADHD (Attention Deficit Hyperactivity Disorder)",
                category: "developmental",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "4-18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Prefrontal Cortex", "Basal Ganglia", "Attention Networks", "Executive Control Centers", "Motor Control Areas"],
                neurotransmitters: ["Neurotransmitter Balance", "Dopamine/Serotonin Markers", "Neural Pathway Efficiency", "Norepinephrine", "GABA"],
                dsm: "DSM-5: 314.01",
                description: "Child-focused protocol targeting attention, hyperactivity, and impulse control through gentle neurotransmitter optimization.",
                frequencies: ["10 Hz", "14 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor attention span and hyperactivity. May improve focus and reduce impulsivity. Coordinate with behavioral interventions and school support."
            },
            {
                id: 10,
                name: "Epilepsy / Childhood Seizure Disorders",
                category: "neurological",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Cerebral Cortex", "Hippocampus", "Seizure Focus Areas", "Neural Networks", "Brainstem"],
                neurotransmitters: ["Neural Excitability Markers", "Neurotransmitters (GABA, Glutamate)", "Ion Channel Function", "Seizure Threshold", "Neural Stability"],
                dsm: "ICD-10: G40.9",
                description: "Careful seizure reduction protocol targeting neural hyperexcitability and promoting brain stability in children.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "REQUIRES NEUROLOGIST SUPERVISION. Monitor EEG changes. May reduce seizure frequency. Never replace anticonvulsant medications. Emergency protocols ready."
            },
            {
                id: 11,
                name: "Developmental Delay",
                category: "developmental",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "Birth - 6 years",
                primarySystems: "Nervous System / Multiple Systems",
                regions: ["Brain Regions (Cortex, Cerebellum)", "Motor Development Centers", "Language Areas", "Cognitive Processing Centers", "Sensory Integration Areas"],
                neurotransmitters: ["Neurotransmitter Markers", "Endocrine/Metabolic Screening", "Growth Factors", "Neural Development Markers", "Musculoskeletal Function"],
                dsm: "ICD-10: F88",
                description: "Supportive protocol enhancing neuroplasticity and developmental milestones in children with global developmental delays.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor developmental milestones. May support cognitive and motor development. Coordinate with early intervention services and therapies."
            },
            {
                id: 12,
                name: "Cerebral Palsy",
                category: "neurological",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Nervous System / Musculoskeletal System",
                regions: ["Motor Cortex", "Basal Ganglia", "Cerebellum", "Skeletal Muscles", "Bones/Joints", "Spinal Cord"],
                neurotransmitters: ["Neuromuscular Junction Function", "Motor Control Markers", "Muscle Tone Regulators", "Movement Coordination", "Spasticity Markers"],
                dsm: "ICD-10: G80.9",
                description: "Supportive protocol for motor function, muscle tone regulation, and neuroplasticity enhancement in children with cerebral palsy.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor muscle tone and movement. May improve motor control and reduce spasticity. Coordinate with physical therapy, occupational therapy, and neurology."
            },

            // Gastrointestinal & Nutritional Conditions
            {
                id: 13,
                name: "Pediatric Food Allergies",
                category: "immune",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "6 months - 18 years",
                primarySystems: "Digestive System / Immune System",
                regions: ["Stomach Lining", "Small Intestine Villi", "Gut-Associated Lymphoid Tissue (GALT)", "Liver", "Immune System"],
                neurotransmitters: ["IgE/IgA Markers", "B-Lymphocytes System", "IgG/IgA/IgM Levels", "T-Lymphocytes System", "Cytokine Profile (IL-2, IL-6, TNF-α)", "IL-8 System"],
                dsm: "ICD-10: T78.1",
                description: "Protocol addressing food allergies (milk, gluten, peanuts, etc.) through immune tolerance and gut barrier support in children.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor for allergic reactions. May support immune tolerance development. Coordinate with pediatric allergist. Keep emergency medications available."
            },
            {
                id: 14,
                name: "Celiac Disease",
                category: "digestive",
                severity: "moderate",
                duration: "30 minutes",
                ageGroup: "6 months - 18 years",
                primarySystems: "Digestive System / Immune System",
                regions: ["Small Intestine Villi", "Gut-Associated Lymphoid Tissue", "Intestinal Barrier", "Liver", "Pancreas"],
                neurotransmitters: ["IgA Antibodies (Anti-tTG, Anti-Gliadin)", "B-Lymphocytes System", "T-Lymphocytes System", "IL-1 System", "Cytokine Profile (IL-2, IL-6, TNF-α)", "Intestinal Permeability"],
                dsm: "ICD-10: K90.0",
                description: "Protocol supporting intestinal healing and immune regulation in children with celiac disease on gluten-free diet.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Must maintain strict gluten-free diet. Monitor growth and nutritional status. May support intestinal healing. Coordinate with pediatric gastroenterologist."
            },
            {
                id: 15,
                name: "Lactose Intolerance",
                category: "digestive",
                severity: "mild",
                duration: "20 minutes",
                ageGroup: "2-18 years",
                primarySystems: "Digestive System",
                regions: ["Lactase Enzyme Activity", "Small Intestine Mucosa", "Digestive System", "Gut Microbiome"],
                neurotransmitters: ["Microbiome Markers", "Digestive Enzymes", "Lactase Function", "Gut Health Indicators", "Fermentation Markers"],
                dsm: "ICD-10: E73.9",
                description: "Protocol supporting lactase enzyme function and digestive comfort in children with lactose intolerance.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor digestive symptoms after dairy consumption. May improve lactose tolerance. Combine with dietary modifications and enzyme supplements."
            },
            {
                id: 16,
                name: "Infant Colic",
                category: "digestive",
                severity: "moderate",
                duration: "15 minutes",
                ageGroup: "2 weeks - 4 months",
                primarySystems: "Digestive System / Nervous System",
                regions: ["Stomach/Intestine Motility", "Gut Microbiome", "Enteric Nervous System", "Vagus Nerve", "Digestive Tract"],
                neurotransmitters: ["Neurotransmitter Markers", "Inflammatory Markers", "Gut-Brain Axis", "Digestive Hormones", "Microbiome Balance"],
                dsm: "ICD-10: R10.83",
                description: "Very gentle protocol for excessive crying and digestive discomfort in infants, targeting gut-brain axis regulation.",
                frequencies: ["8 Hz", "10 Hz", "304 Hz", "528 Hz"],
                notes: "Use VERY gentle intensity for infants. Monitor crying patterns. May reduce colic episodes. Coordinate with pediatrician. Support with feeding modifications."
            },
            {
                id: 17,
                name: "Reflux (GERD in children)",
                category: "digestive",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Digestive System / Esophagus / Stomach",
                regions: ["Lower Esophageal Sphincter Function", "Stomach Lining", "Esophagus Mucosa", "Diaphragm", "Gastric System"],
                neurotransmitters: ["pH Balance", "Gastric Enzymes", "Sphincter Function", "Digestive Motility", "Acid Production"],
                dsm: "ICD-10: K21.9",
                description: "Gentle protocol targeting esophageal sphincter function and gastric acid regulation in children with reflux.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor feeding patterns and weight gain. May reduce reflux episodes. Coordinate with pediatric gastroenterologist. Support with positioning and diet."
            },

            // Common Childhood Health Issues
            {
                id: 18,
                name: "Frequent Colds & Viral Infections",
                category: "infectious",
                severity: "mild",
                duration: "20 minutes",
                ageGroup: "6 months - 12 years",
                primarySystems: "Respiratory / Immune System",
                regions: ["Nasal Mucosa", "Pharynx", "Bronchi", "Lymphoid Tissue", "Upper Respiratory Tract"],
                neurotransmitters: ["T/B Cells", "B-Lymphocytes System", "T-Lymphocytes System", "NK Cells System", "IgG/IgA/IgM Levels", "Interferon Response"],
                dsm: "ICD-10: J06.9",
                description: "Immune-boosting protocol for children with frequent upper respiratory infections, targeting immune system strengthening.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor infection frequency. May reduce cold duration and frequency. Support with proper nutrition, sleep, and hygiene practices."
            },
            {
                id: 19,
                name: "Pediatric Migraines",
                category: "neurological",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "5-18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Cerebral Cortex", "Vascular System in Brain", "Trigeminal System", "Brainstem", "Pain Processing Centers"],
                neurotransmitters: ["Neurotransmitters (Serotonin, Dopamine)", "Pain Pathway Markers", "Vascular Function", "Neuroinflammation", "CGRP"],
                dsm: "ICD-10: G43.9",
                description: "Protocol targeting migraine prevention and pain reduction in children through neurovascular regulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor headache frequency and triggers. May reduce migraine frequency. Coordinate with pediatric neurology. Support with lifestyle modifications."
            },
            {
                id: 20,
                name: "Sleep Disorders (night terrors, bedwetting, insomnia)",
                category: "sleep",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "2-16 years",
                primarySystems: "Nervous System / Brain / Urinary System",
                regions: ["Brainstem", "Hypothalamus", "Pineal Gland (Melatonin)", "Kidneys/Bladder Function", "Sleep Centers"],
                neurotransmitters: ["Neurotransmitters", "Hormonal Balance", "Sleep Regulation", "Circadian Rhythm", "Bladder Control"],
                dsm: "ICD-10: G47.9",
                description: "Comprehensive sleep protocol addressing various pediatric sleep disorders through circadian rhythm and nervous system regulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Evening sessions recommended. Monitor sleep diary. May improve sleep quality and reduce night terrors. Combine with sleep hygiene education."
            },
            {
                id: 21,
                name: "Childhood Obesity",
                category: "endocrine",
                severity: "moderate",
                duration: "30 minutes",
                ageGroup: "2-18 years",
                primarySystems: "Endocrine / Metabolic / Musculoskeletal System",
                regions: ["Adipose Tissue", "Pancreas (Insulin)", "Liver (Lipid Metabolism)", "Skeletal Muscle", "Hypothalamus"],
                neurotransmitters: ["Hormonal Markers (Leptin, Ghrelin, Insulin)", "Metabolic Function", "Appetite Regulation", "Energy Balance", "Growth Hormones"],
                dsm: "ICD-10: E66.9",
                description: "Protocol supporting healthy metabolism and appetite regulation in children with obesity through hormonal balance.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor BMI and metabolic markers. May support healthy weight management. Coordinate with pediatric endocrinologist and nutritionist."
            },
            {
                id: 22,
                name: "Anemia (Iron Deficiency)",
                category: "hematological",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "6 months - 18 years",
                primarySystems: "Blood / Hematologic System",
                regions: ["Bone Marrow", "RBC Production", "Hemoglobin", "Nutrient Absorption Sites (Duodenum)", "Spleen"],
                neurotransmitters: ["Iron Metabolism Markers (Ferritin, Transferrin)", "Erythropoietin", "Hematopoietic Factors", "Oxygen Transport", "Energy Metabolism"],
                dsm: "ICD-10: D50.9",
                description: "Protocol supporting iron absorption, red blood cell production, and energy levels in children with iron deficiency anemia.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor hemoglobin levels and energy. May support iron absorption and red cell production. Coordinate with pediatrician for iron supplementation."
            },

            // Additional Common Pediatric Conditions
            {
                id: 23,
                name: "Chronic Constipation",
                category: "digestive",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "6 months - 16 years",
                primarySystems: "Digestive System",
                regions: ["Colon", "Rectum", "Pelvic Floor", "Enteric Nervous System", "Anal Sphincter"],
                neurotransmitters: ["Digestive Motility", "Gut-Brain Axis", "Neurotransmitter Balance", "Fiber Processing", "Hydration Markers"],
                dsm: "ICD-10: K59.0",
                description: "Protocol supporting healthy bowel function and digestive motility in children with chronic constipation through gut-brain axis regulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor bowel movement frequency and consistency. May improve digestive motility. Support with dietary fiber, hydration, and toileting routine."
            },

            // Comprehensive Digestive & Nutritional Conditions
            {
                id: 53,
                name: "Irritable Bowel Syndrome (IBS) in Children",
                category: "digestive",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "4-18 years",
                primarySystems: "Digestive System / Nervous System",
                regions: ["Small Intestine", "Colon", "Enteric Nervous System", "Gut-Brain Axis", "Visceral Sensory Pathways"],
                neurotransmitters: ["Gut-Brain Communication", "Serotonin (Gut)", "Visceral Hypersensitivity", "Motility Regulation", "Stress Response"],
                dsm: "ICD-10: K58.9",
                description: "Protocol addressing functional bowel disorder in children with abdominal pain, bloating, and altered bowel habits through gut-brain axis regulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor pain patterns and bowel habits. May reduce visceral hypersensitivity. Support with stress management and dietary modifications."
            },
            {
                id: 54,
                name: "Inflammatory Bowel Disease (Crohn's/Ulcerative Colitis)",
                category: "digestive",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "5-18 years",
                primarySystems: "Digestive System / Immune System",
                regions: ["Small Intestine", "Colon", "Intestinal Wall", "Gut-Associated Lymphoid Tissue", "Mesenteric Lymph Nodes"],
                neurotransmitters: ["Inflammatory Cytokines (TNF-α, IL-6)", "T-Lymphocytes System", "Intestinal Barrier Function", "Mucosal Healing", "Immune Tolerance"],
                dsm: "ICD-10: K50.9/K51.9",
                description: "Comprehensive protocol for pediatric IBD targeting intestinal inflammation reduction and mucosal healing through immune modulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES GASTROENTEROLOGY SUPERVISION. Monitor inflammation markers and growth. May support mucosal healing. Never replace immunosuppressive therapy."
            },
            {
                id: 55,
                name: "Chronic Diarrhea",
                category: "digestive",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "6 months - 18 years",
                primarySystems: "Digestive System / Immune System",
                regions: ["Small Intestine", "Colon", "Intestinal Mucosa", "Gut Microbiome", "Electrolyte Balance Centers"],
                neurotransmitters: ["Fluid Balance", "Electrolyte Regulation", "Intestinal Absorption", "Microbiome Balance", "Inflammatory Control"],
                dsm: "ICD-10: K59.1",
                description: "Protocol addressing persistent diarrhea in children through intestinal function restoration and fluid balance regulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor hydration status and electrolytes. May improve intestinal absorption. Rule out infectious causes. Support with rehydration therapy."
            },
            {
                id: 56,
                name: "Malabsorption Syndrome",
                category: "digestive",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Digestive System / Nutritional System",
                regions: ["Small Intestine Villi", "Pancreas", "Liver", "Bile Ducts", "Intestinal Enzymes"],
                neurotransmitters: ["Digestive Enzymes", "Nutrient Absorption", "Pancreatic Function", "Bile Production", "Intestinal Permeability"],
                dsm: "ICD-10: K90.9",
                description: "Comprehensive protocol supporting nutrient absorption and digestive enzyme function in children with malabsorption disorders.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor growth and nutritional status. May improve nutrient absorption. Coordinate with pediatric gastroenterologist and nutritionist."
            },
            {
                id: 57,
                name: "Protein-Energy Malnutrition (PEM)",
                category: "digestive",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "6 months - 5 years",
                primarySystems: "Nutritional System / Multiple Systems",
                regions: ["Digestive System", "Muscle Tissue", "Liver", "Immune System", "Growth Centers"],
                neurotransmitters: ["Protein Synthesis", "Growth Factors", "Metabolic Function", "Immune Function", "Nutritional Markers"],
                dsm: "ICD-10: E46",
                description: "Critical protocol supporting protein and energy metabolism in malnourished children through comprehensive nutritional restoration.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES IMMEDIATE MEDICAL SUPERVISION. Monitor vital signs and refeeding syndrome. May support nutritional recovery. Coordinate with pediatric nutrition team."
            },
            {
                id: 58,
                name: "Vitamin D Deficiency/Rickets",
                category: "digestive",
                severity: "moderate",
                duration: "30 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Nutritional System / Musculoskeletal System",
                regions: ["Bones", "Parathyroid Glands", "Kidneys", "Intestinal Absorption", "Growth Plates"],
                neurotransmitters: ["Vitamin D Metabolism", "Calcium Absorption", "Phosphate Balance", "Bone Formation", "Parathyroid Hormone"],
                dsm: "ICD-10: E55.9",
                description: "Protocol supporting vitamin D metabolism and calcium absorption in children with deficiency-related bone disorders.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor bone health and growth. May support vitamin D utilization. Coordinate with pediatric endocrinologist. Support with supplementation."
            },
            {
                id: 59,
                name: "Iron Deficiency (Non-Anemic)",
                category: "digestive",
                severity: "mild",
                duration: "25 minutes",
                ageGroup: "6 months - 18 years",
                primarySystems: "Nutritional System / Hematologic System",
                regions: ["Duodenum", "Iron Storage Sites", "Bone Marrow", "Liver", "Spleen"],
                neurotransmitters: ["Iron Absorption", "Ferritin Storage", "Transferrin Function", "Heme Synthesis", "Energy Metabolism"],
                dsm: "ICD-10: E61.1",
                description: "Protocol supporting iron absorption and storage in children with iron deficiency before anemia develops.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor ferritin levels and energy. May improve iron absorption. Support with iron-rich foods and vitamin C. Rule out blood loss."
            },
            {
                id: 60,
                name: "Zinc Deficiency",
                category: "digestive",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "6 months - 18 years",
                primarySystems: "Nutritional System / Immune System",
                regions: ["Small Intestine", "Immune System", "Skin", "Growth Centers", "Wound Healing Sites"],
                neurotransmitters: ["Zinc Absorption", "Immune Function", "Protein Synthesis", "Growth Factors", "Antioxidant Systems"],
                dsm: "ICD-10: E60",
                description: "Protocol supporting zinc absorption and utilization in children with deficiency affecting growth and immunity.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor growth and immune function. May improve zinc absorption. Support with zinc-rich foods. Watch for skin and hair changes."
            },
            {
                id: 61,
                name: "B-Vitamin Deficiencies",
                category: "digestive",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "6 months - 18 years",
                primarySystems: "Nutritional System / Nervous System",
                regions: ["Small Intestine", "Nervous System", "Red Blood Cells", "Energy Metabolism Centers", "Liver"],
                neurotransmitters: ["B-Vitamin Absorption", "Energy Metabolism", "Neurotransmitter Synthesis", "DNA Synthesis", "Methylation Pathways"],
                dsm: "ICD-10: E53.9",
                description: "Protocol supporting B-vitamin absorption and metabolism in children with deficiencies affecting energy and neurological function.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor energy levels and neurological symptoms. May improve B-vitamin utilization. Support with balanced nutrition and supplementation."
            },
            {
                id: 62,
                name: "Failure to Thrive (Nutritional)",
                category: "digestive",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "Birth - 5 years",
                primarySystems: "Nutritional System / Growth System",
                regions: ["Digestive System", "Growth Centers", "Hypothalamus", "Liver", "Muscle Tissue"],
                neurotransmitters: ["Growth Hormone", "IGF-1", "Nutritional Absorption", "Metabolic Function", "Appetite Regulation"],
                dsm: "ICD-10: R62.51",
                description: "Comprehensive protocol addressing poor growth due to nutritional factors through metabolic optimization and appetite enhancement.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES PEDIATRIC SUPERVISION. Monitor growth charts closely. May support nutritional utilization. Rule out organic causes. Coordinate with nutrition team."
            },
            {
                id: 63,
                name: "Feeding Disorders (Infants/Toddlers)",
                category: "digestive",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "Birth - 3 years",
                primarySystems: "Digestive System / Nervous System",
                regions: ["Oral Motor System", "Swallowing Centers", "Esophagus", "Sensory Processing Areas", "Appetite Centers"],
                neurotransmitters: ["Oral Motor Coordination", "Swallowing Reflex", "Sensory Processing", "Appetite Regulation", "Feeding Behavior"],
                dsm: "ICD-10: F98.2",
                description: "Gentle protocol supporting feeding skills and oral motor development in infants and toddlers with feeding difficulties.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor weight gain and feeding tolerance. May improve oral motor skills. Coordinate with feeding therapy and pediatric nutrition."
            },
            {
                id: 64,
                name: "Cyclic Vomiting Syndrome",
                category: "digestive",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "3-18 years",
                primarySystems: "Digestive System / Nervous System",
                regions: ["Stomach", "Vomiting Centers (Medulla)", "Hypothalamus", "Autonomic Nervous System", "Gut-Brain Axis"],
                neurotransmitters: ["Nausea/Vomiting Control", "Autonomic Balance", "Stress Response", "Gastric Motility", "Neurotransmitter Balance"],
                dsm: "ICD-10: G43.A0",
                description: "Protocol targeting recurrent vomiting episodes in children through autonomic nervous system regulation and stress response modulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor episode frequency and triggers. May reduce vomiting episodes. Often stress-related. Support with trigger avoidance and stress management."
            },
            {
                id: 65,
                name: "Gastroparesis",
                category: "digestive",
                severity: "moderate",
                duration: "30 minutes",
                ageGroup: "5-18 years",
                primarySystems: "Digestive System / Nervous System",
                regions: ["Stomach", "Vagus Nerve", "Gastric Smooth Muscle", "Enteric Nervous System", "Pyloric Sphincter"],
                neurotransmitters: ["Gastric Motility", "Vagal Function", "Smooth Muscle Coordination", "Digestive Hormones", "Autonomic Balance"],
                dsm: "ICD-10: K31.84",
                description: "Protocol supporting gastric emptying and motility in children with delayed stomach emptying through neural pathway enhancement.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor gastric emptying and symptoms. May improve motility. Often associated with diabetes. Coordinate with pediatric gastroenterologist."
            },
            {
                id: 66,
                name: "Peptic Ulcer Disease (H. pylori)",
                category: "digestive",
                severity: "moderate",
                duration: "30 minutes",
                ageGroup: "5-18 years",
                primarySystems: "Digestive System / Immune System",
                regions: ["Stomach Lining", "Duodenum", "Gastric Mucosa", "Immune Response Centers", "Acid Production Sites"],
                neurotransmitters: ["Mucosal Protection", "Acid Regulation", "Immune Response", "Healing Factors", "Bacterial Resistance"],
                dsm: "ICD-10: K27.9",
                description: "Protocol supporting mucosal healing and immune response in children with H. pylori-related peptic ulcers alongside antibiotic treatment.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES ANTIBIOTIC TREATMENT. Monitor pain and healing. May support mucosal repair. Coordinate with pediatric gastroenterologist."
            },
            {
                id: 67,
                name: "Short Bowel Syndrome",
                category: "digestive",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Digestive System / Nutritional System",
                regions: ["Remaining Small Intestine", "Colon", "Liver", "Pancreas", "Intestinal Adaptation Sites"],
                neurotransmitters: ["Intestinal Adaptation", "Nutrient Absorption", "Digestive Hormones", "Gut Trophic Factors", "Metabolic Function"],
                dsm: "ICD-10: K91.2",
                description: "Comprehensive protocol supporting intestinal adaptation and nutrient absorption in children with surgically shortened bowel.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES SPECIALIZED MEDICAL CARE. Monitor nutritional status closely. May support intestinal adaptation. Coordinate with pediatric surgery and nutrition."
            },
            {
                id: 68,
                name: "Hirschsprung Disease",
                category: "digestive",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Birth - 5 years",
                primarySystems: "Digestive System / Nervous System",
                regions: ["Colon", "Rectum", "Enteric Nervous System", "Anal Sphincter", "Bowel Wall Muscles"],
                neurotransmitters: ["Enteric Nerve Function", "Bowel Motility", "Sphincter Control", "Neural Development", "Digestive Coordination"],
                dsm: "ICD-10: Q43.1",
                description: "Supportive protocol for children with congenital absence of enteric nerves, targeting bowel function optimization post-surgery.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Usually requires surgery. May support post-surgical bowel function. Monitor for enterocolitis. Coordinate with pediatric surgery."
            },
            {
                id: 69,
                name: "Intussusception (Recurrent)",
                category: "digestive",
                severity: "severe",
                duration: "25 minutes",
                ageGroup: "6 months - 5 years",
                primarySystems: "Digestive System / Musculoskeletal System",
                regions: ["Small Intestine", "Colon", "Intestinal Wall Muscles", "Mesenteric Vessels", "Bowel Motility Centers"],
                neurotransmitters: ["Intestinal Motility", "Smooth Muscle Coordination", "Vascular Function", "Pain Pathways", "Digestive Rhythm"],
                dsm: "ICD-10: K56.1",
                description: "Preventive protocol for children with history of intussusception, targeting intestinal motility regulation and recurrence prevention.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "EMERGENCY CONDITION when acute. May help prevent recurrence. Monitor for abdominal pain and vomiting. Immediate medical care for acute episodes."
            },
            {
                id: 70,
                name: "Biliary Atresia",
                category: "digestive",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "Birth - 2 years",
                primarySystems: "Digestive System / Liver System",
                regions: ["Bile Ducts", "Liver", "Gallbladder", "Hepatic Function", "Biliary Tree"],
                neurotransmitters: ["Bile Flow", "Liver Function", "Bilirubin Metabolism", "Hepatic Regeneration", "Digestive Function"],
                dsm: "ICD-10: Q44.2",
                description: "Supportive protocol for infants with bile duct obstruction, targeting liver function support and bile flow optimization.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES IMMEDIATE SURGICAL INTERVENTION. May support liver function post-surgery. Monitor jaundice and growth. Coordinate with pediatric hepatology."
            },
            {
                id: 71,
                name: "Necrotizing Enterocolitis (NEC)",
                category: "digestive",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Premature infants",
                primarySystems: "Digestive System / Immune System",
                regions: ["Small Intestine", "Colon", "Intestinal Wall", "Mesenteric Circulation", "Gut Barrier Function"],
                neurotransmitters: ["Intestinal Barrier", "Inflammatory Control", "Tissue Healing", "Immune Balance", "Gut Protection"],
                dsm: "ICD-10: P77.9",
                description: "Critical supportive protocol for premature infants with intestinal inflammation, targeting tissue protection and healing.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "NICU EMERGENCY CONDITION. Supportive only alongside intensive medical care. May support healing. Coordinate with neonatology team."
            },
            {
                id: 72,
                name: "Functional Dyspepsia",
                category: "digestive",
                severity: "mild",
                duration: "20 minutes",
                ageGroup: "8-18 years",
                primarySystems: "Digestive System / Nervous System",
                regions: ["Stomach", "Duodenum", "Vagus Nerve", "Gastric Sensory Pathways", "Gut-Brain Axis"],
                neurotransmitters: ["Gastric Sensitivity", "Digestive Comfort", "Stress Response", "Gastric Motility", "Visceral Sensation"],
                dsm: "ICD-10: K30",
                description: "Protocol addressing functional stomach discomfort in children through gastric sensitivity reduction and stress management.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor symptoms and stress triggers. May reduce gastric hypersensitivity. Support with stress management and dietary modifications."
            },
            {
                id: 73,
                name: "Rumination Disorder",
                category: "digestive",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "3 months - 2 years",
                primarySystems: "Digestive System / Behavioral System",
                regions: ["Esophagus", "Stomach", "Oral Motor System", "Behavioral Control Centers", "Feeding Centers"],
                neurotransmitters: ["Feeding Behavior", "Oral Motor Control", "Digestive Rhythm", "Behavioral Regulation", "Sensory Processing"],
                dsm: "DSM-5: 307.53",
                description: "Behavioral-digestive protocol addressing repeated regurgitation and re-chewing in infants through feeding behavior modification.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor feeding patterns and weight. May support normal feeding behavior. Coordinate with behavioral therapy and pediatric gastroenterology."
            },
            {
                id: 24,
                name: "Failure to Thrive",
                category: "endocrine",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Birth - 5 years",
                primarySystems: "Endocrine / Multiple Systems",
                regions: ["Hypothalamus", "Pituitary Gland", "Growth Plates", "Digestive System", "Thyroid"],
                neurotransmitters: ["Growth Hormone", "IGF-1", "Thyroid Hormones", "Insulin", "Nutritional Markers"],
                dsm: "ICD-10: R62.51",
                description: "Comprehensive protocol supporting growth and development in children with failure to thrive through hormonal and nutritional optimization.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES PEDIATRIC SUPERVISION. Monitor growth charts and nutritional status. May support healthy weight gain. Coordinate with pediatric endocrinologist."
            },
            {
                id: 25,
                name: "Juvenile Diabetes (Type 1)",
                category: "endocrine",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "6 months - 18 years",
                primarySystems: "Endocrine / Metabolic System",
                regions: ["Pancreatic Beta Cells", "Liver", "Muscle Tissue", "Adipose Tissue", "Kidneys"],
                neurotransmitters: ["Insulin", "Glucagon", "C-Peptide", "Autoantibodies", "Glucose Metabolism"],
                dsm: "ICD-10: E10.9",
                description: "Supportive protocol for pancreatic function and glucose regulation in children with Type 1 diabetes, targeting beta cell preservation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "NEVER REPLACE INSULIN THERAPY. Monitor blood glucose closely. May support pancreatic function. Coordinate with pediatric endocrinologist. Emergency protocols ready."
            },
            {
                id: 26,
                name: "Congenital Heart Defects",
                category: "cardiovascular",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Cardiovascular System",
                regions: ["Heart Chambers", "Heart Valves", "Great Vessels", "Cardiac Conduction System", "Myocardium"],
                neurotransmitters: ["Cardiac Function Markers", "Circulation Efficiency", "Oxygen Transport", "Cardiac Enzymes", "Vascular Function"],
                dsm: "ICD-10: Q24.9",
                description: "Gentle supportive protocol for children with congenital heart defects, targeting cardiac function optimization and circulation support.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "REQUIRES CARDIOLOGY SUPERVISION. Monitor cardiac function and oxygen saturation. May support heart function. Never replace cardiac medications."
            },
            {
                id: 27,
                name: "Scoliosis (Adolescent Idiopathic)",
                category: "musculoskeletal",
                severity: "moderate",
                duration: "30 minutes",
                ageGroup: "10-18 years",
                primarySystems: "Musculoskeletal System",
                regions: ["Spinal Column", "Paraspinal Muscles", "Ribs", "Pelvis", "Postural Control Centers"],
                neurotransmitters: ["Postural Control", "Muscle Balance", "Spinal Alignment", "Growth Factors", "Proprioception"],
                dsm: "ICD-10: M41.9",
                description: "Protocol supporting spinal alignment and muscle balance in adolescents with idiopathic scoliosis through postural control enhancement.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor spinal curvature progression. May support postural control. Coordinate with orthopedic specialist and physical therapy. Regular X-ray monitoring."
            },
            {
                id: 28,
                name: "Enuresis (Bedwetting)",
                category: "urogenital",
                severity: "mild",
                duration: "20 minutes",
                ageGroup: "5-12 years",
                primarySystems: "Urinary System / Nervous System",
                regions: ["Bladder", "Urethral Sphincter", "Pons", "Hypothalamus", "Spinal Cord"],
                neurotransmitters: ["Bladder Control", "Sleep Regulation", "Hormonal Balance", "Neurological Function", "Maturation Markers"],
                dsm: "ICD-10: N39.44",
                description: "Gentle protocol supporting bladder control and sleep-wake regulation in children with nocturnal enuresis.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor dry nights frequency. May improve bladder control. Support with behavioral interventions and fluid management. Avoid shame or punishment."
            },
            {
                id: 29,
                name: "Tourette Syndrome",
                category: "neurological",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "2-18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Basal Ganglia", "Frontal Cortex", "Caudate Nucleus", "Putamen", "Motor Cortex"],
                neurotransmitters: ["Motor Control", "Tic Regulation", "Neurotransmitter Balance", "Impulse Control", "Movement Coordination"],
                dsm: "DSM-5: 307.23",
                description: "Protocol targeting tic reduction and motor control in children with Tourette syndrome through basal ganglia regulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor tic frequency and severity. May reduce tic intensity. Coordinate with pediatric neurology. Support with stress management and behavioral therapy."
            },
            {
                id: 30,
                name: "Selective Mutism",
                category: "behavioral",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "3-8 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Amygdala", "Broca's Area", "Anterior Cingulate", "Prefrontal Cortex", "Language Centers"],
                neurotransmitters: ["Anxiety Regulation", "Social Communication", "Fear Response", "Language Processing", "Emotional Control"],
                dsm: "DSM-5: 312.23",
                description: "Gentle protocol addressing social anxiety and communication barriers in children with selective mutism through anxiety reduction.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor speaking in different settings. May reduce social anxiety. Coordinate with speech therapy and child psychology. Use very gentle approach."
            },
            {
                id: 31,
                name: "Oppositional Defiant Disorder (ODD)",
                category: "behavioral",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "3-12 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Prefrontal Cortex", "Amygdala", "Anterior Cingulate", "Orbitofrontal Cortex", "Limbic System"],
                neurotransmitters: ["Emotional Regulation", "Impulse Control", "Behavioral Control", "Stress Response", "Social Processing"],
                dsm: "DSM-5: 313.81",
                description: "Protocol targeting emotional regulation and impulse control in children with oppositional defiant disorder through prefrontal enhancement.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor behavioral episodes and emotional regulation. May improve impulse control. Coordinate with behavioral therapy and family counseling."
            },
            {
                id: 32,
                name: "Separation Anxiety Disorder",
                category: "anxiety",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "6 months - 12 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Amygdala", "Hippocampus", "Prefrontal Cortex", "Hypothalamus", "Attachment Centers"],
                neurotransmitters: ["Anxiety Regulation", "Attachment Security", "Stress Response", "Emotional Stability", "Fear Processing"],
                dsm: "DSM-5: 309.21",
                description: "Gentle protocol reducing separation anxiety and promoting secure attachment in children through stress response regulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor separation tolerance and anxiety symptoms. May reduce distress during separations. Support with gradual exposure and attachment work."
            },
            {
                id: 33,
                name: "Pica (Non-food Eating)",
                category: "behavioral",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "12 months - 6 years",
                primarySystems: "Nervous System / Digestive System",
                regions: ["Orbitofrontal Cortex", "Insula", "Basal Ganglia", "Sensory Processing Areas", "Reward Centers"],
                neurotransmitters: ["Sensory Regulation", "Impulse Control", "Nutritional Balance", "Behavioral Control", "Reward Processing"],
                dsm: "DSM-5: 307.52",
                description: "Protocol addressing non-food eating behaviors in children through sensory regulation and nutritional balance support.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor eating behaviors and nutritional status. May reduce pica episodes. Check for nutritional deficiencies. Ensure environmental safety."
            },
            {
                id: 34,
                name: "Reactive Attachment Disorder",
                category: "developmental",
                severity: "severe",
                duration: "25 minutes",
                ageGroup: "9 months - 5 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Amygdala", "Hippocampus", "Orbitofrontal Cortex", "Attachment Centers", "Stress Response System"],
                neurotransmitters: ["Attachment Security", "Emotional Regulation", "Stress Response", "Social Bonding", "Trust Development"],
                dsm: "DSM-5: 313.89",
                description: "Careful protocol supporting attachment formation and emotional regulation in children with reactive attachment disorder.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "REQUIRES TRAUMA-INFORMED CARE. Monitor attachment behaviors. May support emotional regulation. Coordinate with attachment therapy and trauma specialists."
            },
            {
                id: 35,
                name: "Childhood Apraxia of Speech",
                category: "developmental",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "18 months - 8 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Motor Cortex", "Broca's Area", "Cerebellum", "Basal Ganglia", "Speech Motor Areas"],
                neurotransmitters: ["Speech Motor Planning", "Language Processing", "Motor Coordination", "Neural Connectivity", "Speech Development"],
                dsm: "ICD-10: F80.1",
                description: "Protocol supporting speech motor planning and coordination in children with childhood apraxia of speech through neural pathway enhancement.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor speech clarity and motor planning. May improve speech coordination. Coordinate with speech-language pathology. Support with motor practice."
            },
            {
                id: 36,
                name: "Sensory Processing Disorder",
                category: "developmental",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "2-12 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Sensory Cortex", "Thalamus", "Brainstem", "Cerebellum", "Vestibular System"],
                neurotransmitters: ["Sensory Integration", "Sensory Processing", "Neural Regulation", "Sensory Modulation", "Adaptive Response"],
                dsm: "ICD-10: F88",
                description: "Protocol supporting sensory integration and processing in children with sensory processing difficulties through neural regulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor sensory responses and behaviors. May improve sensory tolerance. Coordinate with occupational therapy. Support with sensory diet."
            },
            {
                id: 37,
                name: "Pediatric Anxiety Disorders",
                category: "anxiety",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "3-18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Amygdala", "Prefrontal Cortex", "Hippocampus", "Anterior Cingulate", "Hypothalamus"],
                neurotransmitters: ["Anxiety Regulation", "Stress Response", "Emotional Control", "Fear Processing", "Calm Response"],
                dsm: "DSM-5: F41.9",
                description: "Gentle protocol reducing anxiety symptoms and promoting emotional regulation in children through stress response modulation.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor anxiety symptoms and coping. May reduce worry and fear responses. Support with relaxation techniques and cognitive behavioral strategies."
            },
            {
                id: 38,
                name: "Childhood Depression",
                category: "mood",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "6-18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Prefrontal Cortex", "Limbic System", "Hippocampus", "Anterior Cingulate", "Reward Centers"],
                neurotransmitters: ["Mood Regulation", "Emotional Balance", "Neurotransmitter Function", "Energy Regulation", "Motivation"],
                dsm: "DSM-5: F32.9",
                description: "Protocol supporting mood regulation and emotional well-being in children with depression through neurotransmitter balance.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor mood and energy levels. May improve emotional regulation. REQUIRES mental health supervision. Support with therapy and family involvement."
            },
            {
                id: 39,
                name: "Pediatric Bipolar Disorder",
                category: "mood",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "6-18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Prefrontal Cortex", "Limbic System", "Amygdala", "Hypothalamus", "Circadian Centers"],
                neurotransmitters: ["Mood Stabilization", "Circadian Regulation", "Emotional Balance", "Neural Stability", "Sleep-Wake Cycle"],
                dsm: "DSM-5: F31.9",
                description: "Careful protocol supporting mood stabilization and circadian regulation in children with bipolar disorder through neural balance.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "REQUIRES PSYCHIATRIC SUPERVISION. Monitor mood cycles and sleep. May support mood stability. Never replace mood stabilizers. Emergency protocols ready."
            },
            {
                id: 40,
                name: "Intellectual Disability",
                category: "developmental",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Frontal Cortex", "Hippocampus", "Cerebellum", "Language Areas", "Motor Areas"],
                neurotransmitters: ["Cognitive Function", "Learning Capacity", "Neural Development", "Adaptive Skills", "Brain Plasticity"],
                dsm: "DSM-5: F70-F79",
                description: "Supportive protocol enhancing cognitive function and adaptive skills in children with intellectual disability through neuroplasticity promotion.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor developmental progress and adaptive skills. May support cognitive development. Coordinate with special education and developmental services."
            },
            {
                id: 41,
                name: "Fetal Alcohol Spectrum Disorders",
                category: "developmental",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Nervous System / Brain",
                regions: ["Frontal Cortex", "Corpus Callosum", "Cerebellum", "Hippocampus", "Basal Ganglia"],
                neurotransmitters: ["Neural Development", "Brain Function", "Cognitive Processing", "Behavioral Regulation", "Neural Repair"],
                dsm: "ICD-10: Q86.0",
                description: "Comprehensive protocol supporting brain development and function in children with fetal alcohol spectrum disorders through neural repair.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor developmental milestones and behaviors. May support neural development. Coordinate with developmental pediatrics and special services."
            },
            {
                id: 42,
                name: "Spina Bifida",
                category: "neurological",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Nervous System / Musculoskeletal System",
                regions: ["Spinal Cord", "Neural Tube", "Motor Neurons", "Sensory Pathways", "Bladder Control Centers"],
                neurotransmitters: ["Neural Function", "Motor Control", "Sensory Processing", "Spinal Cord Function", "Neuroplasticity"],
                dsm: "ICD-10: Q05.9",
                description: "Supportive protocol for children with spina bifida, targeting neural function optimization and mobility support through spinal cord enhancement.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor motor and sensory function. May support neural connectivity. Coordinate with neurosurgery, urology, and rehabilitation services."
            },
            {
                id: 43,
                name: "Muscular Dystrophy (Duchenne)",
                category: "musculoskeletal",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "2-18 years",
                primarySystems: "Musculoskeletal System",
                regions: ["Skeletal Muscle", "Cardiac Muscle", "Dystrophin Protein Complex", "Motor Neurons", "Muscle Fibers"],
                neurotransmitters: ["Muscle Function", "Protein Synthesis", "Muscle Preservation", "Cellular Repair", "Motor Function"],
                dsm: "ICD-10: G71.0",
                description: "Supportive protocol for boys with Duchenne muscular dystrophy, targeting muscle preservation and function through cellular support.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor muscle strength and function. May support muscle preservation. Coordinate with neuromuscular specialist, cardiology, and physical therapy."
            },
            {
                id: 44,
                name: "Cystic Fibrosis",
                category: "respiratory",
                severity: "severe",
                duration: "35 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Respiratory System / Digestive System",
                regions: ["Lungs", "Pancreas", "Liver", "Intestines", "Sweat Glands"],
                neurotransmitters: ["CFTR Protein Function", "Cellular Transport", "Respiratory Function", "Digestive Function", "Mucus Clearance"],
                dsm: "ICD-10: E84.9",
                description: "Comprehensive protocol supporting respiratory and digestive function in children with cystic fibrosis through cellular transport enhancement.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES SPECIALIZED MEDICAL CARE. Monitor lung function and nutrition. May support cellular function. Coordinate with CF care team."
            },
            {
                id: 45,
                name: "Down Syndrome",
                category: "genetic",
                severity: "moderate",
                duration: "30 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Nervous System / Multiple Systems",
                regions: ["Frontal Cortex", "Hippocampus", "Cerebellum", "Heart", "Immune System"],
                neurotransmitters: ["Cognitive Development", "Immune Function", "Cardiac Function", "Neural Development", "Health Optimization"],
                dsm: "ICD-10: Q90.9",
                description: "Supportive protocol enhancing cognitive development and health in children with Down syndrome through neural and immune support.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor developmental progress and health issues. May support cognitive development. Coordinate with developmental pediatrics and therapies."
            },
            {
                id: 46,
                name: "RSV (Respiratory Syncytial Virus)",
                category: "infectious",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "Birth - 2 years (most critical)",
                primarySystems: "Respiratory System / Immune System",
                regions: ["Lower Respiratory Tract", "Bronchioles", "Alveoli", "Upper Airways", "Lymphoid Tissue", "Nasal Passages"],
                neurotransmitters: ["Antiviral Response", "T/B Cells", "Interferon System", "NK Cells System", "Respiratory Function", "Inflammatory Control"],
                dsm: "ICD-10: J21.0",
                description: "Gentle antiviral protocol for infants and toddlers with RSV infection, targeting respiratory support and immune enhancement.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES PEDIATRIC SUPERVISION. Monitor breathing closely. May reduce severity and duration. Keep oxygen saturation monitoring available. Coordinate with pediatric pulmonologist for severe cases."
            },
            {
                id: 47,
                name: "Acute Bronchitis",
                category: "respiratory",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "2-18 years",
                primarySystems: "Respiratory System / Immune System",
                regions: ["Bronchi", "Bronchial Mucosa", "Lower Airways", "Trachea", "Respiratory Epithelium"],
                neurotransmitters: ["Inflammatory Response", "Mucus Production", "Ciliary Function", "Immune Response", "Respiratory Recovery"],
                dsm: "ICD-10: J20.9",
                description: "Protocol for acute bronchial inflammation in children, targeting airway healing and mucus clearance through gentle respiratory support.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor cough and breathing patterns. May reduce inflammation and support recovery. Usually viral - avoid unnecessary antibiotics. Support with hydration and humidity."
            },
            {
                id: 48,
                name: "Chronic Bronchitis",
                category: "respiratory",
                severity: "moderate",
                duration: "30 minutes",
                ageGroup: "5-18 years",
                primarySystems: "Respiratory System / Immune System",
                regions: ["Bronchi", "Bronchial Walls", "Mucus Glands", "Respiratory Epithelium", "Lower Airways"],
                neurotransmitters: ["Chronic Inflammation Control", "Mucus Regulation", "Airway Repair", "Immune Balance", "Respiratory Function"],
                dsm: "ICD-10: J41.0",
                description: "Long-term protocol for persistent bronchial inflammation in children, targeting airway remodeling and chronic inflammation reduction.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "Monitor for underlying causes (asthma, allergies, environmental factors). May reduce chronic symptoms. Coordinate with pediatric pulmonologist for comprehensive care."
            },
            {
                id: 49,
                name: "Bronchiolitis",
                category: "respiratory",
                severity: "moderate",
                duration: "25 minutes",
                ageGroup: "Birth - 2 years",
                primarySystems: "Respiratory System / Immune System",
                regions: ["Bronchioles", "Small Airways", "Alveolar Ducts", "Lower Respiratory Tract", "Lung Parenchyma"],
                neurotransmitters: ["Small Airway Function", "Viral Response", "Inflammatory Control", "Oxygen Exchange", "Respiratory Recovery"],
                dsm: "ICD-10: J21.9",
                description: "Gentle protocol for small airway inflammation in infants and toddlers, commonly caused by RSV, targeting bronchiolar healing.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES CLOSE MONITORING. Watch for breathing difficulty and oxygen saturation. May support recovery. Often requires hospitalization in severe cases."
            },
            {
                id: 50,
                name: "Pediatric Pneumonia",
                category: "respiratory",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Birth - 18 years",
                primarySystems: "Respiratory System / Immune System",
                regions: ["Lung Alveoli", "Lung Parenchyma", "Pleura", "Bronchi", "Pulmonary Circulation"],
                neurotransmitters: ["Infection Response", "Inflammatory Control", "Oxygen Transport", "Immune Function", "Tissue Healing"],
                dsm: "ICD-10: J18.9",
                description: "Supportive protocol for lung infection in children, targeting immune response and respiratory function alongside medical treatment.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES IMMEDIATE MEDICAL CARE. Monitor vital signs closely. Supportive only - never replace antibiotics. Coordinate with pediatric emergency/pulmonology."
            },
            {
                id: 51,
                name: "Croup (Laryngotracheobronchitis)",
                category: "respiratory",
                severity: "moderate",
                duration: "20 minutes",
                ageGroup: "6 months - 6 years",
                primarySystems: "Respiratory System / Upper Airways",
                regions: ["Larynx", "Trachea", "Upper Bronchi", "Vocal Cords", "Subglottic Area"],
                neurotransmitters: ["Airway Inflammation", "Vocal Cord Function", "Upper Airway Patency", "Viral Response", "Swelling Reduction"],
                dsm: "ICD-10: J05.0",
                description: "Protocol for viral upper airway inflammation causing characteristic barking cough in young children, targeting airway swelling reduction.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz"],
                notes: "Monitor for stridor and breathing difficulty. May reduce airway swelling. Cool mist helpful. Seek emergency care if severe breathing difficulty develops."
            },
            {
                id: 52,
                name: "Whooping Cough (Pertussis)",
                category: "infectious",
                severity: "severe",
                duration: "30 minutes",
                ageGroup: "Birth - 18 years (most severe in infants)",
                primarySystems: "Respiratory System / Immune System",
                regions: ["Respiratory Epithelium", "Bronchi", "Trachea", "Ciliary System", "Immune Response Centers"],
                neurotransmitters: ["Bacterial Response", "Ciliary Function", "Cough Reflex", "Immune Recovery", "Respiratory Healing"],
                dsm: "ICD-10: A37.9",
                description: "Supportive protocol for pertussis bacterial infection, targeting respiratory recovery and immune support alongside antibiotic treatment.",
                frequencies: ["8 Hz", "10 Hz", "40 Hz", "304 Hz", "528 Hz", "727 Hz"],
                notes: "REQUIRES IMMEDIATE MEDICAL CARE. Highly contagious - isolation needed. Supportive only alongside antibiotics. Monitor for apnea in infants. Vaccination prevention crucial."
            }

        ];

        let filteredProtocols = [...protocols];

        // Helper functions for detailed protocol information
        function getRegionDetails(region) {
            const details = {
                'Amygdala': 'Fear processing, emotional memory, threat detection',
                'Prefrontal Cortex': 'Executive control, decision-making, emotional regulation',
                'Hippocampus': 'Memory consolidation, spatial navigation, stress response',
                'Hypothalamus': 'Homeostasis, circadian rhythm, stress hormone regulation',
                'Basal Ganglia': 'Motor control, habit formation, reward processing',
                'Limbic System': 'Emotional processing, motivation, memory formation',
                'Brainstem': 'Vital functions, arousal, neurotransmitter production',
                'Temporal Lobe': 'Auditory processing, language, memory storage',
                'Anterior Cingulate': 'Attention, emotion regulation, conflict monitoring',
                'Cerebellum': 'Motor coordination, cognitive function, emotional regulation',
                'Pineal Gland': 'Melatonin production, circadian rhythm regulation',
                'Suprachiasmatic Nucleus': 'Master circadian clock, sleep-wake cycles',
                'Locus Coeruleus': 'Norepinephrine production, arousal, attention',
                'Orbitofrontal Cortex': 'Decision-making, impulse control, social behavior',
                'Caudate Nucleus': 'Goal-directed behavior, habit formation',
                'Insula': 'Interoception, emotional awareness, empathy',
                'Visual Cortex': 'Visual processing, perception',
                'Motor Cortex': 'Voluntary movement control',
                'Somatosensory Cortex': 'Touch, pain, temperature sensation',
                'Parietal Cortex': 'Spatial processing, attention',
                'Nucleus Accumbens': 'Reward processing, motivation',
                'Periaqueductal Gray': 'Pain modulation, defensive behaviors',
                'Skeletal Muscle': 'Voluntary movement, posture, strength, myocyte viability',
                'Cardiac Muscle': 'Heart contraction, circulation, myocardial protection',
                'Dystrophin Protein Complex': 'Muscle fiber structural integrity, sarcolemma stabilization',
                'Middle Ear Structures (Ossicles, Tympanic Membrane)': 'Sound transmission, hearing function, pressure regulation',
                'Eustachian Tube': 'Middle ear pressure equalization, drainage function',
                'Cochlea': 'Sound processing, frequency detection, auditory transduction',
                'Auditory Nerve Pathways': 'Sound signal transmission to brain, hearing processing',
                'Lymphoid Tissue (Adenoids, Tonsils)': 'Immune defense, pathogen filtering, antibody production'
            };
            return details[region] || 'Neural processing and regulation';
        }

        function getNeurotransmitterDetails(nt) {
            const details = {
                'Serotonin': 'Mood regulation, sleep, appetite, impulse control',
                'Dopamine': 'Reward, motivation, motor control, attention',
                'GABA': 'Inhibitory control, anxiety reduction, sleep promotion',
                'Norepinephrine': 'Alertness, arousal, stress response, attention',
                'Acetylcholine': 'Memory, learning, attention, muscle control',
                'Glutamate': 'Excitatory transmission, learning, memory formation',
                'Melatonin': 'Sleep-wake cycle, circadian rhythm regulation',
                'Cortisol': 'Stress response, inflammation, metabolism',
                'Adenosine': 'Sleep pressure, fatigue signaling',
                'Orexin': 'Wakefulness, appetite, arousal',
                'Endorphins': 'Pain relief, pleasure, reward',
                'Leptin': 'Appetite suppression, energy balance',
                'Calcium': 'Muscle contraction, cellular signaling, homeostasis',
                'Growth Factors': 'Tissue repair, muscle regeneration, cellular growth',
                'T/B Cells': 'Adaptive immunity, antibody production, immune memory',
                'IgA': 'Mucosal immunity, first-line defense, pathogen neutralization',
                'Middle Ear Function': 'Sound conduction, pressure regulation, hearing clarity',
                'Auditory Processing': 'Sound interpretation, frequency discrimination, hearing comprehension',
                'Immune Response': 'Pathogen defense, inflammation control, healing promotion',
                'B-Lymphocytes System': 'Adaptive immune response, antibody production, neuro-immune signaling',
                'T-Lymphocytes System': 'Cell-mediated immunity, immune-neuro communication regulation',
                'NK Cells System': 'Innate immunity, viral surveillance, neurochemical signaling influence',
                'CRP System': 'Inflammatory response marker, acute phase inflammation, CNS impact',
                'IL-1 System': 'Pro-inflammatory cytokine, neural activity modulation, neuroimmune interactions',
                'IL-8 System': 'Chemokine inflammation, neutrophil recruitment, neural-glial communication',
                'B-cell Count & Activity': 'B-lymphocyte function, antibody production capacity, immune memory',
                'IgG/IgA/IgM Levels': 'Immunoglobulin status, humoral immunity, pathogen protection',
                'T-cell Subtypes (CD4, CD8)': 'Helper and cytotoxic T-cells, immune coordination, cellular immunity',
                'Cytokine Profile (IL-2, IL-6, TNF-α)': 'Inflammatory mediators, immune signaling, CNS communication',
                'NK Cell Activity': 'Natural killer cell function, viral defense, tumor surveillance',
                'C-reactive Protein Levels': 'Acute inflammation marker, systemic immune activation',
                'IL-1α, IL-1β Levels': 'Interleukin-1 inflammatory response, neural activity modulation',
                'IL-8 Concentration': 'Chemokine levels, inflammatory recruitment, neural communication'
            };
            return details[nt] || 'Neurochemical balance and signaling';
        }

        function getSpecificEtalons(category) {
            const etalons = {
                'anxiety': ['Fear response', 'Worry patterns', 'Panic triggers', 'Avoidance behaviors', 'Physical tension', 'Breathing patterns'],
                'mood': ['Mood stability', 'Energy levels', 'Motivation', 'Sleep patterns', 'Appetite regulation', 'Cognitive clarity'],
                'developmental': ['Attention span', 'Impulse control', 'Social interaction', 'Learning capacity', 'Motor coordination', 'Sensory processing'],
                'neurological': ['Neural stability', 'Seizure threshold', 'Motor control', 'Sensory processing', 'Cognitive function', 'Neuroplasticity'],
                'infectious': ['Immune function', 'Pathogen resistance', 'Inflammation control', 'Recovery speed', 'Tissue healing', 'Barrier function'],
                'respiratory': ['Breathing efficiency', 'Airway function', 'Gas exchange', 'Lung capacity', 'Respiratory rhythm', 'Oxygen saturation'],
                'digestive': ['Digestive motility', 'Nutrient absorption', 'Gut barrier', 'Microbiome balance', 'Enzyme function', 'pH regulation'],
                'immune': ['Immune tolerance', 'Allergic response', 'Inflammatory balance', 'Antibody function', 'Cellular immunity', 'Immune memory'],
                'skin': ['Barrier function', 'Moisture balance', 'Inflammatory response', 'Healing capacity', 'Sensitivity threshold', 'Protective function'],
                'musculoskeletal': ['Joint mobility', 'Muscle strength', 'Bone density', 'Movement coordination', 'Pain threshold', 'Structural integrity'],
                'behavioral': ['Emotional regulation', 'Impulse control', 'Social skills', 'Attention focus', 'Behavioral flexibility', 'Stress tolerance'],
                'cardiovascular': ['Heart rhythm', 'Blood pressure', 'Circulation efficiency', 'Cardiac output', 'Vascular function', 'Oxygen delivery'],
                'genetic': ['Gene expression', 'Cellular function', 'Metabolic pathways', 'Protein synthesis', 'DNA repair', 'Epigenetic factors'],
                'urogenital': ['Bladder control', 'Kidney function', 'Urinary flow', 'Hormonal balance', 'Reproductive health', 'Fluid balance'],
                'sleep': ['Sleep initiation', 'Sleep maintenance', 'Sleep quality', 'Circadian alignment', 'Sleep anxiety', 'Arousal regulation'],
                'endocrine': ['Hormone balance', 'Metabolic rate', 'Growth factors', 'Insulin sensitivity', 'Thyroid function', 'Adrenal function'],
                'hematological': ['Blood cell production', 'Oxygen transport', 'Iron metabolism', 'Clotting function', 'Immune cell activity', 'Nutrient transport']
            };
            return etalons[category] || ['General function', 'Stress response', 'Adaptation', 'Balance', 'Regulation', 'Recovery'];
        }

        function renderProtocols() {
            const grid = document.getElementById('protocolGrid');
            grid.innerHTML = '';

            filteredProtocols.forEach(protocol => {
                const card = document.createElement('div');
                card.className = `bg-white rounded-lg shadow-md card-hover cursor-pointer category-${protocol.category}`;
                card.onclick = () => openModal(protocol);
                
                card.innerHTML = `
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-4">
                            <h3 class="text-lg font-semibold text-gray-900">${protocol.name}</h3>
                            <span class="severity-indicator severity-${protocol.severity}"></span>
                        </div>
                        
                        <div class="text-xs text-purple-600 font-medium mb-2">${protocol.dsm}</div>
                        <div class="text-xs text-blue-600 font-medium mb-2">👶 Age: ${protocol.ageGroup}</div>
                        <div class="text-xs text-green-600 font-medium mb-3">🎯 ${protocol.primarySystems}</div>
                        
                        <p class="text-gray-600 text-sm mb-4">${protocol.description}</p>
                        
                        <div class="flex flex-wrap gap-2 mb-4">
                            ${protocol.regions.slice(0, 2).map(region => 
                                `<span class="px-2 py-1 bg-purple-100 text-purple-700 text-xs rounded-full">🧠 ${region}</span>`
                            ).join('')}
                            ${protocol.regions.length > 2 ? `<span class="text-xs text-gray-500">+${protocol.regions.length - 2} more</span>` : ''}
                        </div>
                        
                        <div class="flex justify-between items-center text-sm text-gray-500 mb-3">
                            <span>⏱️ ${protocol.duration}</span>
                            <span>${protocol.frequencies.length} frequencies</span>
                        </div>
                        
                        <div class="flex flex-wrap gap-1">
                            ${protocol.frequencies.slice(0, 3).map(freq => 
                                `<span class="frequency-badge">${freq}</span>`
                            ).join('')}
                            ${protocol.frequencies.length > 3 ? `<span class="text-xs text-gray-500">+${protocol.frequencies.length - 3} more</span>` : ''}
                        </div>
                    </div>
                `;
                
                grid.appendChild(card);
            });

            // Update total count
            document.getElementById('totalProtocols').textContent = filteredProtocols.length;
        }

        function openModal(protocol) {
            document.getElementById('modalTitle').textContent = protocol.name;
            document.getElementById('modalCategory').textContent = protocol.category.charAt(0).toUpperCase() + protocol.category.slice(1) + ' Condition • Age: ' + protocol.ageGroup;
            document.getElementById('modalDSM').textContent = protocol.dsm;
            
            // Get the modal content container and replace with comprehensive blueprint
            const modalContentContainer = document.getElementById('modalContent');
            modalContentContainer.innerHTML = `
                <div class="space-y-6">
                    <!-- 1. Title and Overview -->
                    <div class="bg-gradient-to-r from-purple-50 to-blue-50 p-6 rounded-lg border border-purple-200">
                        <h3 class="text-xl font-bold text-purple-800 mb-4">📋 1. Title and Overview</h3>
                        <div class="space-y-4">
                            <div>
                                <h4 class="font-semibold text-gray-800 mb-2">What it is:</h4>
                                <p class="text-gray-700">${protocol.description}</p>
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-800 mb-2">Primary Body Systems Affected:</h4>
                                <p class="text-gray-700 font-medium text-green-700">${protocol.primarySystems}</p>
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-800 mb-2">How it affects the body:</h4>
                                <p class="text-gray-700">Leads to fatigue, cognitive impairment, mood disturbance, reduced immunity, and increased risk of metabolic and cardiovascular imbalance. Comprehensive neurological and physiological impacts affecting multiple body systems, emotional regulation, and overall quality of life.</p>
                            </div>
                        </div>
                    </div>

                    <!-- 2. Related Body Parts/Systems -->
                    <div class="bg-gradient-to-r from-blue-50 to-green-50 p-6 rounded-lg border border-blue-200">
                        <h3 class="text-xl font-bold text-blue-800 mb-4">🎯 2. Related Body Parts/Systems & Associated Etalons to Test</h3>
                        
                        <div class="space-y-4">
                            <div class="bg-white p-4 rounded-lg border border-blue-200">
                                <h4 class="font-semibold text-blue-700 mb-3">Category: Primary Body Regions</h4>
                                <div class="space-y-2 text-sm">
                                    ${protocol.regions.map(region => `<div>• <strong>${region}</strong> → ${getRegionDetails(region)}</div>`).join('')}
                                </div>
                            </div>
                            
                            <div class="bg-white p-4 rounded-lg border border-blue-200">
                                <h4 class="font-semibold text-blue-700 mb-3">Category: Biochemical & Functional Markers</h4>
                                <div class="space-y-2 text-sm">
                                    ${protocol.neurotransmitters.map(nt => `<div>• <strong>${nt}</strong> → ${getNeurotransmitterDetails(nt)}</div>`).join('')}
                                </div>
                            </div>
                            
                            <div class="bg-white p-4 rounded-lg border border-blue-200">
                                <h4 class="font-semibold text-blue-700 mb-3">Category: Specific Etalons</h4>
                                <div class="grid grid-cols-2 gap-2 text-sm">
                                    ${getSpecificEtalons(protocol.category).map(etalon => `<div class="bg-blue-50 px-3 py-1 rounded">• ${etalon}</div>`).join('')}
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- 3. Energetic Markers -->
                    <div class="bg-gradient-to-r from-green-50 to-yellow-50 p-6 rounded-lg border border-green-200">
                        <h3 class="text-xl font-bold text-green-800 mb-4">🔍 3. Energetic Markers to Look For (NLS Analysis)</h3>
                        
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div class="space-y-3">
                                <div class="bg-white p-3 rounded border border-green-200">
                                    <h5 class="font-semibold text-green-700 mb-2">Visual Icons (Flandler's scale):</h5>
                                    <p class="text-sm text-gray-700">Brown/Red on ${protocol.regions[0]} → ${protocol.category} dysregulation</p>
                                </div>
                                
                                <div class="bg-white p-3 rounded border border-green-200">
                                    <h5 class="font-semibold text-green-700 mb-2">Graph Numbers:</h5>
                                    <p class="text-sm text-gray-700">${protocol.severity === 'mild' ? '2–4' : protocol.severity === 'moderate' ? '3–5' : '4–6'} (unstable ${protocol.category} regulation)</p>
                                </div>
                                
                                <div class="bg-white p-3 rounded border border-green-200">
                                    <h5 class="font-semibold text-green-700 mb-2">Blue vs Red Lines:</h5>
                                    <p class="text-sm text-gray-700">Divergence in ${protocol.neurotransmitters.join('/')} rhythms</p>
                                </div>
                            </div>
                            
                            <div class="space-y-3">
                                <div class="bg-white p-3 rounded border border-green-200">
                                    <h5 class="font-semibold text-green-700 mb-2">Isoline:</h5>
                                    <p class="text-sm text-gray-700">Fluctuations matching disrupted ${protocol.category} cycles</p>
                                </div>
                                
                                <div class="bg-white p-3 rounded border border-green-200">
                                    <h5 class="font-semibold text-green-700 mb-2">KCC (Spectral Similarity):</h5>
                                    <p class="text-sm text-gray-700">Low to ${protocol.neurotransmitters.join(', ')} sets indicates dysregulation</p>
                                </div>
                                
                                <div class="bg-white p-3 rounded border border-green-200">
                                    <h5 class="font-semibold text-green-700 mb-2">Entropy (E) & Vegetative Test:</h5>
                                    <p class="text-sm text-gray-700">E ~${protocol.severity === 'mild' ? '2–4' : protocol.severity === 'moderate' ? '3–5' : '4–6'} in ${protocol.regions[0]} = ${protocol.category} stress<br>+10% with ${protocol.category} rhythm or ${protocol.neurotransmitters[0]} sets indicates positive balance</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- 4. Recommended Protocol -->
                    <div class="bg-gradient-to-r from-yellow-50 to-orange-50 p-6 rounded-lg border border-yellow-200">
                        <h3 class="text-xl font-bold text-yellow-800 mb-4">⚡ 4. Recommended Energetic Protocol</h3>
                        
                        <div class="space-y-4">
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                <div class="bg-white p-4 rounded border border-yellow-200">
                                    <h5 class="font-semibold text-yellow-700 mb-2">Initial Scan</h5>
                                    <p class="text-sm text-gray-700">General pediatric ${protocol.category === 'mood' ? 'neuropsychiatric' : protocol.category === 'sleep' ? 'neuroendocrine + circadian rhythm' : protocol.category} scan (40–50% intensity for children).</p>
                                </div>
                                
                                <div class="bg-white p-4 rounded border border-yellow-200">
                                    <h5 class="font-semibold text-yellow-700 mb-2">Focused Analysis</h5>
                                    <p class="text-sm text-gray-700">${protocol.regions.join(', ')}, associated pathways.</p>
                                </div>
                            </div>
                            
                            <div class="bg-white p-4 rounded border border-yellow-200">
                                <h5 class="font-semibold text-yellow-700 mb-3">Meta-Therapy – Selection</h5>
                                <div class="grid grid-cols-2 gap-2">
                                    <div class="bg-yellow-50 px-3 py-1 rounded text-sm">• ${protocol.category} regulation</div>
                                    <div class="bg-yellow-50 px-3 py-1 rounded text-sm">• ${protocol.neurotransmitters[0]} balancing</div>
                                    <div class="bg-yellow-50 px-3 py-1 rounded text-sm">• Gentle stress reduction</div>
                                    <div class="bg-yellow-50 px-3 py-1 rounded text-sm">• Age-appropriate stabilization</div>
                                </div>
                            </div>
                            
                            <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                                <div class="bg-white p-3 rounded border border-yellow-200">
                                    <h5 class="font-semibold text-yellow-700 mb-2">Meta-Therapy Settings</h5>
                                    <p class="text-sm text-gray-700">${protocol.severity === 'mild' ? 'Very gentle mode' : protocol.severity === 'moderate' ? 'Gentle intensity' : 'Careful gentle progression'}; 1–3 min cycles for children.</p>
                                </div>
                                
                                <div class="bg-white p-3 rounded border border-yellow-200">
                                    <h5 class="font-semibold text-yellow-700 mb-2">Sessions</h5>
                                    <p class="text-sm text-gray-700">${protocol.severity === 'mild' ? '1-2 cycles × 1-2 times/week' : protocol.severity === 'moderate' ? '2 cycles × 2 times/week' : '2-3 cycles × 2-3 times/week'} (reassess every 2 weeks).</p>
                                </div>
                                
                                <div class="bg-white p-3 rounded border border-yellow-200">
                                    <h5 class="font-semibold text-yellow-700 mb-2">Focus</h5>
                                    <p class="text-sm text-gray-700">≤2 priority etalons per session (avoid child overload).</p>
                                </div>
                            </div>
                            
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                <div class="bg-white p-3 rounded border border-yellow-200">
                                    <h5 class="font-semibold text-yellow-700 mb-2">Vegetative Test</h5>
                                    <p class="text-sm text-gray-700">${getSpecificEtalons(protocol.category)[0]} + ${getSpecificEtalons(protocol.category)[1]} support.</p>
                                </div>
                                
                                <div class="bg-white p-3 rounded border border-yellow-200">
                                    <h5 class="font-semibold text-yellow-700 mb-2">Imprinting</h5>
                                    <p class="text-sm text-gray-700">Water, ${protocol.category === 'sleep' ? 'chamomile tea' : 'child-safe herbal tea'}, or crystal → imprint "${protocol.category} balance" etalons.</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- 5. Client Instructions -->
                    <div class="bg-gradient-to-r from-orange-50 to-red-50 p-6 rounded-lg border border-orange-200">
                        <h3 class="text-xl font-bold text-orange-800 mb-4">👤 5. Client Instructions (Parent/Guardian)</h3>
                        <div class="space-y-3">
                            <div class="flex items-start"><span class="text-orange-600 mr-2">•</span><span class="text-gray-700">${protocol.category === 'sleep' ? 'Maintain child sleep hygiene (dark room, no screens before bed, consistent bedtime routine)' : 'Maintain consistent daily routines and age-appropriate stress management practices'}</span></div>
                            <div class="flex items-start"><span class="text-orange-600 mr-2">•</span><span class="text-gray-700">Use imprinted remedy ${protocol.category === 'sleep' ? 'before child\'s sleep' : 'as directed'} (3–5 min gentle relaxation for child)</span></div>
                            <div class="flex items-start"><span class="text-orange-600 mr-2">•</span><span class="text-gray-700">Supportive lifestyle measures: ${protocol.category === 'sleep' ? 'reduce child caffeine, gentle bedtime routine, calming activities' : 'proper child nutrition, age-appropriate exercise, adequate sleep'}</span></div>
                            <div class="flex items-start"><span class="text-orange-600 mr-2">•</span><span class="text-gray-700">Monitor child symptoms and report any significant changes to pediatrician</span></div>
                            <div class="flex items-start"><span class="text-orange-600 mr-2">•</span><span class="text-gray-700">Continue all prescribed pediatric medications and coordinate with healthcare providers</span></div>
                            <div class="flex items-start"><span class="text-orange-600 mr-2">•</span><span class="text-gray-700">Ensure child comfort during sessions - allow breaks, use gentle positioning</span></div>
                        </div>
                    </div>

                    <!-- 6. Medical Disclaimer -->
                    <div class="bg-gradient-to-r from-red-50 to-pink-50 p-6 rounded-lg border border-red-200">
                        <h3 class="text-xl font-bold text-red-800 mb-4">⚠️ 6. Important Pediatric Medical Disclaimer and Follow-up</h3>
                        
                        <div class="space-y-4">
                            <div class="bg-white p-4 rounded border border-red-200">
                                <h5 class="font-semibold text-red-700 mb-2">Critical Pediatric Medical Need:</h5>
                                <p class="text-sm text-gray-700">This protocol is complementary only for children. ${protocol.name} may indicate underlying pediatric medical conditions ${protocol.category === 'sleep' ? '(e.g., sleep apnea, anxiety, developmental issues)' : ''} that require specialized pediatric care. Always coordinate with qualified pediatric healthcare providers and obtain parental consent.</p>
                            </div>
                            
                            <div class="bg-white p-4 rounded border border-red-200">
                                <h5 class="font-semibold text-red-700 mb-2">Pediatric Follow-up:</h5>
                                <p class="text-sm text-gray-700">Re-scan ${protocol.severity === 'mild' ? 'every 2-3 weeks' : protocol.severity === 'moderate' ? 'bi-weekly (or per symptom change)' : 'weekly'} to track ${protocol.category === 'sleep' ? 'child circadian alignment and sleep quality' : 'child ' + protocol.category + ' regulation and symptom'} trends. Monitor developmental milestones.</p>
                            </div>
                            
                            <div class="bg-red-100 p-3 rounded border border-red-300">
                                <p class="text-red-800 font-medium text-sm">🚨 Pediatric Safety Notes: ${protocol.notes}</p>
                            </div>
                        </div>
                    </div>
                </div>
            `;
            
            document.getElementById('protocolModal').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('protocolModal').classList.add('hidden');
        }

        function filterProtocols() {
            const searchTerm = document.getElementById('searchInput').value.toLowerCase();
            const categoryFilter = document.getElementById('categoryFilter').value;
            const severityFilter = document.getElementById('severityFilter').value;

            filteredProtocols = protocols.filter(protocol => {
                const matchesSearch = protocol.name.toLowerCase().includes(searchTerm) ||
                                    protocol.description.toLowerCase().includes(searchTerm) ||
                                    protocol.regions.some(region => region.toLowerCase().includes(searchTerm)) ||
                                    protocol.neurotransmitters.some(nt => nt.toLowerCase().includes(searchTerm)) ||
                                    protocol.frequencies.some(freq => freq.toLowerCase().includes(searchTerm)) ||
                                    protocol.dsm.toLowerCase().includes(searchTerm) ||
                                    protocol.primarySystems.toLowerCase().includes(searchTerm);
                
                const matchesCategory = !categoryFilter || protocol.category === categoryFilter;
                const matchesSeverity = !severityFilter || protocol.severity === severityFilter;
                
                return matchesSearch && matchesCategory && matchesSeverity;
            });

            renderProtocols();
        }

        // Toggle mapping section
        function toggleMappingSection() {
            const content = document.getElementById('mappingContent');
            const button = document.getElementById('toggleMapping');
            
            if (content.classList.contains('hidden')) {
                content.classList.remove('hidden');
                button.textContent = 'Hide Mapping Guide';
            } else {
                content.classList.add('hidden');
                button.textContent = 'Show Mapping Guide';
            }
        }

        // Event listeners
        document.getElementById('searchInput').addEventListener('input', filterProtocols);
        document.getElementById('categoryFilter').addEventListener('change', filterProtocols);
        document.getElementById('severityFilter').addEventListener('change', filterProtocols);
        document.getElementById('toggleMapping').addEventListener('click', toggleMappingSection);

        // Close modal when clicking outside
        document.getElementById('protocolModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeModal();
            }
        });

        // Initialize
        renderProtocols();
    </script>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-6 mt-12">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <p class="text-sm text-gray-300">© 2025 Anavrin Wellness. All rights reserved.</p>  
        </div>
    </footer>
    // Privacy Policy, Terms of Service, and Copyright Modal Functions
        function showPrivacyPolicy(event) {
            event.preventDefault();
            document.getElementById('privacyModal').classList.remove('hidden');
        }

        function closePrivacyModal() {
            document.getElementById('privacyModal').classList.add('hidden');
        }

        function showTermsOfService(event) {
            event.preventDefault();
            document.getElementById('termsModal').classList.remove('hidden');
        }

        function closeTermsModal() {
            document.getElementById('termsModal').classList.add('hidden');
        }

        function showCopyrightDisclaimer(event) {
            event.preventDefault();
            document.getElementById('copyrightModal').classList.remove('hidden');
        }

        function closeCopyrightModal() {
            document.getElementById('copyrightModal').classList.add('hidden');
        }

        // Close modals on outside click
        document.addEventListener('DOMContentLoaded', function() {
            document.getElementById('privacyModal').addEventListener('click', (e) => {
                if (e.target.id === 'privacyModal') {
                    closePrivacyModal();
                }
            });

            document.getElementById('termsModal').addEventListener('click', (e) => {
                if (e.target.id === 'termsModal') {
                    closeTermsModal();
                }
            });

            document.getElementById('copyrightModal').addEventListener('click', (e) => {
                if (e.target.id === 'copyrightModal') {
                    closeCopyrightModal();
                }
            });
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'979c3169912d73e9',t:'MTc1Njk3NTM0MS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>

<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'975b08d98257b72b',t:'MTc1NjI5MjEwNS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
