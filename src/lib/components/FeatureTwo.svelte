<section class="py-24 bg-[#0b0c0e]">
  <div class="container-custom">
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
      
      <!-- Left Content -->
      <div class="lg:col-span-4 flex flex-col justify-center">
        <h2 class="text-3xl md:text-5xl font-medium tracking-tight mb-12">
          The AppGen platform for operations teams
        </h2>

        <div class="space-y-12 border-l border-[#2e3138] pl-8 relative">
            <div class="group cursor-pointer relative">
                <!-- Active Indicator Line -->
                <div class="absolute -left-8 top-0 bottom-0 w-0.5 bg-white"></div>
                
                <h3 class="text-xs font-bold text-gray-500 mb-2 uppercase tracking-wider">AI & LLMs</h3>
                <p class="text-xl text-white font-medium mb-2">Build agents, workflows, and apps with the power of AI</p>
                <p class="text-gray-400 text-sm leading-relaxed block transition-all">
                    Connect to any model, vector database, or API. Build custom AI tools securely.
                </p>
            </div>

            <div class="group cursor-pointer opacity-50 hover:opacity-100 transition-opacity relative">
                 <!-- Inactive Indicator Line (hidden or transparent) -->
                <div class="absolute -left-8 top-0 bottom-0 w-0.5 bg-transparent group-hover:bg-gray-700 transition-colors"></div>

                <h3 class="text-xs font-bold text-gray-500 mb-2 uppercase tracking-wider">Actionable Insights</h3>
                <p class="text-xl text-white font-medium">Turn data into action</p>
            </div>

            <div class="group cursor-pointer opacity-50 hover:opacity-100 transition-opacity relative">
                 <div class="absolute -left-8 top-0 bottom-0 w-0.5 bg-transparent group-hover:bg-gray-700 transition-colors"></div>
                <h3 class="text-xs font-bold text-gray-500 mb-2 uppercase tracking-wider">Support teams</h3>
                <p class="text-xl text-white font-medium">Drive customer success with effective tools</p>
            </div>
            
             <div class="flex gap-2 mt-8">
                <!-- Small icons/logos -->
                <div class="w-8 h-8 bg-[#1e2025] rounded border border-[#2e3138]"></div>
                <div class="w-8 h-8 bg-[#1e2025] rounded border border-[#2e3138]"></div>
                <div class="w-8 h-8 bg-[#1e2025] rounded border border-[#2e3138]"></div>
                <div class="w-8 h-8 bg-[#1e2025] rounded border border-[#2e3138]"></div>
            </div>
        </div>
      </div>

      <!-- Right Image -->
      <div class="lg:col-span-8">
        <div class="relative rounded-xl overflow-hidden border border-[#2e3138] bg-[#15171b] shadow-2xl">
            <!-- Header of the fake app -->
            <div class="h-12 border-b border-[#2e3138] flex items-center px-4 gap-4">
                <div class="flex gap-1.5">
                    <div class="w-3 h-3 rounded-full bg-red-500/20"></div>
                    <div class="w-3 h-3 rounded-full bg-yellow-500/20"></div>
                    <div class="w-3 h-3 rounded-full bg-green-500/20"></div>
                </div>
                <div class="h-6 w-64 bg-[#1e2025] rounded text-xs flex items-center px-2 text-gray-500">https://retool.com/app/fraud-monitoring</div>
            </div>
            
            <!-- Body of the fake app -->
            <div class="p-6 grid grid-cols-12 gap-6 bg-[#0b0c0e] min-h-[500px]">
                <!-- Workflow visualizer -->
                <div class="col-span-5 bg-[#15171b] rounded border border-[#2e3138] p-4 relative overflow-hidden">
                    <div class="absolute top-4 left-4 text-xs font-mono text-gray-400">Workflow: Freeze Account</div>
                    <!-- Nodes -->
                    <div class="absolute top-20 left-10 w-32 h-16 bg-[#1e2025] border border-blue-500/50 rounded flex items-center justify-center text-xs">Trigger</div>
                    <div class="absolute top-44 left-10 w-32 h-16 bg-[#1e2025] border border-[#2e3138] rounded flex items-center justify-center text-xs">Check Status</div>
                    <div class="absolute top-64 left-40 w-32 h-16 bg-[#1e2025] border border-[#2e3138] rounded flex items-center justify-center text-xs">Update DB</div>
                    
                    <!-- Connecting lines (simplified) -->
                    <svg class="absolute inset-0 w-full h-full pointer-events-none stroke-gray-600">
                        <path d="M74 100 V 176" fill="none" />
                        <path d="M74 240 V 256 H 200 V 270" fill="none" />
                    </svg>
                </div>
                
                <!-- Detail View -->
                <div class="col-span-7 bg-white rounded text-black p-6 font-sans">
                    <div class="flex justify-between items-start mb-6">
                        <h3 class="font-bold text-lg">Fraud Review Portal</h3>
                        <span class="bg-red-100 text-red-700 text-xs px-2 py-1 rounded-full font-bold">High Risk</span>
                    </div>
                    
                    <div class="grid grid-cols-2 gap-y-4 text-sm mb-6">
                        <div class="text-gray-500">Username</div>
                        <div class="font-medium">solo3pc</div>
                        
                        <div class="text-gray-500">Fraud reason</div>
                        <div class="font-medium">Large transaction</div>
                        
                        <div class="text-gray-500">Account status</div>
                        <div class="font-medium text-green-600 bg-green-100 px-2 py-0.5 rounded w-fit">Active</div>
                        
                        <div class="text-gray-500">Date</div>
                        <div class="font-medium">11:40PM 2025-02-27</div>
                    </div>
                    
                    <div class="flex gap-2">
                        <button class="bg-black text-white px-4 py-2 rounded text-sm font-medium w-full">Freeze Account</button>
                        <button class="bg-gray-100 text-black px-4 py-2 rounded text-sm font-medium w-full">File Notice</button>
                    </div>
                </div>
            </div>
        </div>
      </div>
      
    </div>
  </div>
</section>
