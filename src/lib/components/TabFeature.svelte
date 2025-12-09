<script>
    let activeTab = 'Code'; // Default to Code as per screenshot
    const tabs = ['Chat', 'Canvas', 'Code'];
</script>

<section class="py-24 bg-[#0b0c0e]">
    <div class="container-custom">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
            
            <!-- Left Side: Content & Tabs -->
            <div class="lg:col-span-4 flex flex-col justify-center">
                <h2 class="text-3xl md:text-5xl font-medium tracking-tight mb-8">
                    All the ways you work, in one place
                </h2>
                <p class="text-gray-400 mb-12 leading-relaxed">
                    Skip the tab-switching and handoffs. Retool unifies generation, refinement, and logic into a single surface so you can turn ideas into software without breaking your flow.
                </p>

                <div class="space-y-4">
                    {#each tabs as tab}
                        <!-- svelte-ignore a11y-click-events-have-key-events -->
                        <div 
                            class="p-6 rounded-lg border cursor-pointer transition-all duration-200 {activeTab === tab ? 'bg-[#15171b] border-[#2e3138]' : 'border-transparent hover:bg-[#15171b]/50'}"
                            on:click={() => activeTab = tab}
                        >
                            <h3 class="text-xs font-bold text-gray-500 uppercase tracking-wider mb-2">{tab}</h3>
                            {#if tab === 'Chat'}
                                <h4 class="text-lg font-medium text-white mb-1">Go from prompt to production</h4>
                                <p class="text-sm text-gray-400">Describe what you want to build, and let Retool translate your inputs into functional components and logic.</p>
                            {:else if tab === 'Canvas'}
                                <h4 class="text-lg font-medium text-white mb-1">Drag, drop, and shape complex UIs</h4>
                                <p class="text-sm text-gray-400">Use the canvas to lay out real components, experiment with flow, and see structure as you build. It's the fastest way to translate mental models into working software.</p>
                            {:else if tab === 'Code'}
                                <h4 class="text-lg font-medium text-white mb-1">Full customization in code</h4>
                                <p class="text-sm text-gray-400">Write, edit, and debug directly in our IDE and insert custom code anywhere.</p>
                            {/if}
                        </div>
                    {/each}
                </div>
            </div>

            <!-- Right Side: Visual -->
            <div class="lg:col-span-8">
                <div class="relative rounded-xl overflow-hidden border border-[#2e3138] bg-[#15171b] h-full min-h-[600px] shadow-2xl">
                    {#if activeTab === 'Code'}
                        <!-- Fake IDE UI -->
                        <div class="absolute inset-0 flex flex-col">
                            <!-- Toolbar -->
                            <div class="h-10 border-b border-[#2e3138] bg-[#1e2025] flex items-center px-4 justify-between">
                                <div class="flex gap-2">
                                    <div class="w-3 h-3 rounded-full bg-red-500/50"></div>
                                    <div class="w-3 h-3 rounded-full bg-yellow-500/50"></div>
                                    <div class="w-3 h-3 rounded-full bg-green-500/50"></div>
                                </div>
                                <div class="text-xs font-mono text-gray-500">Inventory.js</div>
                            </div>
                            
                            <!-- Code Area -->
                            <div class="flex-1 p-6 font-mono text-sm text-gray-300 overflow-hidden relative">
                                <div class="absolute left-0 top-0 bottom-0 w-12 bg-[#1e2025] border-r border-[#2e3138] text-right pr-3 pt-6 text-gray-600 select-none">
                                    1<br>2<br>3<br>4<br>5<br>6<br>7<br>8<br>9<br>10<br>11<br>12<br>13<br>14<br>15
                                </div>
                                <div class="pl-16 pt-0">
                                    <span class="text-purple-400">import</span> <span class="text-blue-400">{`{ useState, useEffect }`}</span> <span class="text-purple-400">from</span> <span class="text-green-400">'react'</span>;<br>
                                    <br>
                                    <span class="text-purple-400">export default function</span> <span class="text-yellow-200">InventoryManager</span>() {`{`}<br>
                                    &nbsp;&nbsp;<span class="text-purple-400">const</span> [items, setItems] = <span class="text-blue-400">useState</span>([]);<br>
                                    <br>
                                    &nbsp;&nbsp;<span class="text-gray-500">// Fetch inventory data from PostgreSQL</span><br>
                                    &nbsp;&nbsp;<span class="text-purple-400">useEffect</span>(() => {`{`}<br>
                                    &nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-400">queryInventory</span>().<span class="text-blue-400">then</span>(data => <span class="text-blue-400">setItems</span>(data));<br>
                                    &nbsp;&nbsp;{`}`}, []);<br>
                                    <br>
                                    &nbsp;&nbsp;<span class="text-purple-400">return</span> (<br>
                                    &nbsp;&nbsp;&nbsp;&nbsp;&lt;<span class="text-red-400">Table</span><br>
                                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-orange-400">data</span>={'{items}'}<br>
                                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-orange-400">columns</span>={'{['}<br>
                                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{'{ key: "id", name: "ID" },'}<br>
                                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{'{ key: "name", name: "Product Name" },'}<br>
                                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{'{ key: "stock", name: "Stock Level" },'}<br>
                                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{']}'}<br>
                                    &nbsp;&nbsp;&nbsp;&nbsp;/&gt;<br>
                                    &nbsp;&nbsp;);<br>
                                    {`}`}
                                </div>
                                
                                <!-- Floating AI Assistant / Suggestion -->
                                <div class="absolute bottom-10 right-10 w-80 bg-[#1e2025] border border-purple-500/30 rounded-lg shadow-2xl p-4 animate-pulse">
                                    <div class="flex items-center gap-2 mb-2 text-purple-400 text-xs font-bold uppercase">
                                        <svg class="w-3 h-3" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2L2 7l10 5 10-5-10-5zm0 9l2-10 2 10m2-10L2 7l10 5 10-5z"/></svg>
                                        AI Suggestion
                                    </div>
                                    <p class="text-xs text-gray-300">I noticed you're building an inventory table. Would you like to add a "Restock" action button for items with low stock?</p>
                                    <div class="mt-3 flex gap-2">
                                        <button class="bg-purple-600 hover:bg-purple-500 text-white text-xs px-3 py-1.5 rounded">Apply</button>
                                        <button class="bg-[#2e3138] hover:bg-[#3f424a] text-white text-xs px-3 py-1.5 rounded">Dismiss</button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    {:else if activeTab === 'Canvas'}
                        <div class="absolute inset-0 flex items-center justify-center text-gray-500 bg-[#0b0c0e]">
                            <div class="text-center">
                                <div class="w-16 h-16 mx-auto mb-4 border-2 border-dashed border-gray-700 rounded flex items-center justify-center">
                                    <svg class="w-8 h-8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2" ry="2"/><line x1="12" y1="8" x2="12" y2="16"/><line x1="8" y1="12" x2="16" y2="12"/></svg>
                                </div>
                                <p>Canvas Drag & Drop Editor</p>
                            </div>
                        </div>
                    {:else}
                        <div class="absolute inset-0 flex items-center justify-center text-gray-500 bg-[#0b0c0e]">
                             <div class="text-center">
                                <div class="w-16 h-16 mx-auto mb-4 border-2 border-dashed border-gray-700 rounded flex items-center justify-center">
                                    <svg class="w-8 h-8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg>
                                </div>
                                <p>AI Chat Interface</p>
                            </div>
                        </div>
                    {/if}
                </div>
            </div>
            
        </div>
    </div>
</section>
