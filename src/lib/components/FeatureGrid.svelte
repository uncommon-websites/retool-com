<script>
    const features = [
        {
            icon: `<path d="M16 18l6-6-6-6"/><path d="M8 6l-6 6 6 6"/>`,
            title: "Death to boilerplate",
            desc: "LLMs generate mountains of code and multiply complexity, not reduce it. Our composable blocks create the perfect abstraction layer. Focus AI on the 20% that differentiates you, not on reinventing the wheel. What BI did for dashboards, we do for apps."
        },
        {
            icon: `<path d="M8 3v3a2 2 0 0 1-2 2H3m18 0h-3a2 2 0 0 1-2-2V3m0 18v-3a2 2 0 0 1 2-2h3M3 16h3a2 2 0 0 1 2 2v3"/>`,
            title: "Connect everything to anything",
            desc: "Your data, your models, your stack. Retool connects to every source your business relies on — databases, APIs, vector stores, and LLMs. Optimize cost and performance with the best model for every use case."
        },
        {
            icon: `<path d="M21 12V7H5a2 2 0 0 1 0-4h14v4"/><path d="M3 5v14a2 2 0 0 0 2 2h16v-5"/><path d="M18 12a2 2 0 0 0 0 4h4v-4Z"/>`,
            title: "Smarter software—on your terms.",
            desc: "Use Retool's AI-native building blocks to power intelligent behavior in your apps, from LLM responses to workflow automation—backed by the models, data, and logic you choose."
        },
        {
            icon: `<path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/>`,
            title: "Integrate with your dev stack",
            desc: "Connect with standard developer workflows to keep your preferences and best practices with version control, CI/CD, testing, debugging, and maintenance. Deploy and manage across development, staging, and production environments."
        },
        {
            icon: `<rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/>`,
            title: "Secure by default",
            desc: "Enterprise-grade security features and granular permissions protect your sensitive data and ensure compliance. Deploy anywhere with scalable and flexible hosting options — in your cloud or ours."
        },
        {
            icon: `<circle cx="12" cy="12" r="10"/><path d="M12 16v-4"/><path d="M12 8h.01"/>`,
            title: "AI that builds with you",
            desc: "Use natural language to generate queries, logic, and UIs that are schema-aware, contextually grounded, and fully editable. With intelligent assistance built directly into the editor, Retool speeds up development without removing structure, clarity, or oversight."
        }
    ];
</script>

<section class="py-24 bg-[#0b0c0e] border-t border-[#2e3138]">
    <div class="container-custom">
        <h2 class="text-3xl md:text-5xl font-medium tracking-tight mb-16 max-w-2xl">
            How modern teams <br/> ship AI-native software
        </h2>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-12 gap-y-16">
            {#each features as feature}
                <div class="group">
                    <div class="w-10 h-10 mb-6 text-gray-400 group-hover:text-white transition-colors">
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
                            {@html feature.icon}
                        </svg>
                    </div>
                    <h3 class="text-xl font-medium text-white mb-4">{feature.title}</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        {feature.desc}
                    </p>
                </div>
            {/each}
        </div>
    </div>
</section>
