<script lang="ts">
	import { onMount } from 'svelte';

	let scrollY = 0;
</script>

<svelte:window bind:scrollY />

<div class="font-sans text-gray-900 antialiased selection:bg-primary-200 selection:text-primary-900">
	<!-- Navigation / Header -->
    <header class="fixed top-0 left-0 right-0 z-40 bg-white/95 backdrop-blur-sm border-b border-gray-200">
        <div class="px-6 md:px-12 lg:px-24 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <svg class="w-8 h-8 text-gray-900" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M10.1214 2.40967C11.0087 2.40967 11.7683 3.04566 11.9242 3.91908L12.1482 5.17341C12.3042 6.04681 13.0638 6.68282 13.951 6.68282H15.47C17.83 6.68282 19.7432 8.59595 19.7432 10.9559C19.7432 12.3696 19.0567 13.6229 17.999 14.4007C18.4424 14.5514 18.7925 14.7906 19.0496 15.1048C19.3141 15.4514 19.5031 15.9439 19.6165 16.5641C19.6354 16.7283 19.6591 16.8879 19.6827 17.0475C19.7063 17.2071 19.7299 17.3667 19.7488 17.5309C19.7685 17.7014 19.783 17.8473 19.7951 17.9686C19.8062 18.0809 19.8153 18.1721 19.8244 18.2423C19.8622 18.7531 19.9189 19.1726 19.9945 19.4827C20.0742 19.9188 20.2352 20.3438 20.4633 20.7231H17.2352C17.084 20.4313 16.9895 20.0847 16.9139 19.7016C16.8489 19.3722 16.7979 18.9617 16.7368 18.4704C16.7268 18.3904 16.7166 18.3083 16.706 18.2241L16.5926 17.385C16.4981 16.7465 16.3847 16.2905 16.2713 15.9986C16.139 15.725 15.9312 15.5244 15.6476 15.4149C15.3453 15.3055 14.8917 15.2291 14.2491 15.2291H14.1037C13.2164 15.2291 12.4568 14.5931 12.3009 13.7197L12.0769 12.4653C11.9209 11.5919 11.1613 10.9559 10.274 10.9559H7.53417V15.8395H4.48193V2.40967H10.1214ZM16.6909 10.9559C16.6909 11.6302 16.1443 12.1769 15.47 12.1769H13.951C13.0638 12.1769 12.3042 11.5408 12.1482 10.6674L11.9242 9.41312C11.7683 8.53971 11.0087 7.9037 10.1214 7.9037H7.53417V5.46189H10.274C11.1613 5.46189 11.9209 6.0979 12.0769 6.97131L12.3008 8.22563C12.4568 9.09904 13.2164 9.73505 14.1037 9.73505H15.47C16.1443 9.73505 16.6909 10.2817 16.6909 10.9559Z" fill="currentColor"/>
                </svg>
                <span class="font-bold text-xl">Carhartt</span>
            </div>
            <nav class="hidden md:flex items-center gap-8 text-sm font-medium">
                <a href="#collections" class="hover:text-primary-700 transition-colors">Collections</a>
                <a href="#heritage" class="hover:text-primary-700 transition-colors">Heritage</a>
                <a href="#stories" class="hover:text-primary-700 transition-colors">Stories</a>
            </nav>
        </div>
    </header>

	<!-- Hero Section -->
	<section class="relative min-h-screen w-full bg-gray-950 text-white px-6 md:px-12 lg:px-24 pt-32 pb-24 flex items-center overflow-hidden">
		<div class="absolute inset-0 z-0">
			<img src="/generated/image-construction-worker-in-rugged-workwear-o-1765505536451-0.webp" alt="Construction worker in authentic Carhartt workwear" class="w-full h-full object-cover opacity-60" />
			<div class="absolute inset-0 bg-gradient-to-r from-gray-950 via-gray-950/80 to-transparent"></div>
		</div>

		<div class="relative z-10 max-w-4xl">
			<h1 class="font-serif text-5xl md:text-7xl lg:text-8xl leading-[1.1] md:leading-[1.1] tracking-tight mb-8">
				Authentic workwear. Built to last since 1889.
			</h1>
			<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-2xl">
				From construction sites to city streets, Carhartt delivers genuine heritage and uncompromising durability.
			</p>
			<a href="#collections" class="inline-flex items-center justify-center px-8 py-4 bg-primary-600 hover:bg-primary-700 text-white rounded text-sm font-semibold transition-colors duration-300">
				Explore Collections
			</a>
		</div>
	</section>

	<!-- Stockists & Retailers -->
	<section class="bg-white px-6 md:px-12 lg:px-24 py-16 md:py-24">
		<p class="text-lg md:text-xl text-gray-600 mb-12">Available at premium retailers worldwide</p>
		
		<div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4 md:gap-8">
			<!-- Retailer placeholders -->
			{#each ['Urban Outfitters', 'SSENSE', 'END.', 'Dover Street Market', 'Nordstrom', 'Mr Porter'] as retailer}
				<div class="h-20 bg-gray-50 rounded-lg flex items-center justify-center grayscale opacity-60 hover:opacity-100 hover:grayscale-0 transition-all duration-300">
					<span class="font-semibold text-gray-800 text-sm text-center px-2">{retailer}</span>
				</div>
			{/each}
		</div>
	</section>

    <!-- Collections Section -->
    <section class="bg-white px-6 md:px-12 lg:px-24 py-12 md:py-24" id="collections">
        <div class="flex flex-col md:flex-row justify-between items-end mb-16 md:mb-24">
            <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl text-gray-900">Built for work. Made to last.</h2>
            <a href="/collections" class="hidden md:inline-flex items-center text-gray-500 hover:text-gray-900 transition-colors mt-4 md:mt-0">
                View all <span class="ml-2">→</span>
            </a>
        </div>

        <div class="space-y-24 md:space-y-32">
            <!-- Collection 1: Durability -->
            <div class="group grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <div class="lg:col-span-4 space-y-6">
                    <h3 class="font-serif text-3xl md:text-4xl text-gray-900">Uncompromising Durability</h3>
                    <p class="text-gray-600 text-lg leading-relaxed">
                        Every stitch, every seam, every detail engineered for longevity. Our heavy-duty construction and reinforced materials stand up to the toughest conditions.
                    </p>
                    <div class="flex flex-wrap gap-2 pt-2">
                        <span class="px-3 py-1 border border-gray-200 rounded-full text-xs font-medium text-gray-600">Triple-Stitched</span>
                        <span class="px-3 py-1 border border-gray-200 rounded-full text-xs font-medium text-gray-600">Reinforced</span>
                    </div>
                </div>
                <div class="lg:col-span-8">
                    <div class="aspect-[16/9] bg-gray-900 rounded-lg overflow-hidden relative group-hover:scale-[1.02] transition-transform duration-500 ease-out">
                        <img src="/generated/image-close-up-of-durable-workwear-jacket-with-1765505540718-1.webp" alt="Durable workwear construction details" class="w-full h-full object-cover" />
                    </div>
                </div>
            </div>

            <!-- Collection 2: Urban Style -->
            <div class="group grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <div class="lg:col-span-4 space-y-6">
                    <h3 class="font-serif text-3xl md:text-4xl text-gray-900">Urban Fashion Meets Function</h3>
                    <p class="text-gray-600 text-lg leading-relaxed">
                        From Brooklyn streets to downtown studios, authentic workwear that transitions seamlessly from job site to city life.
                    </p>
                    <div class="flex flex-wrap gap-2 pt-2">
                        <span class="px-3 py-1 border border-gray-200 rounded-full text-xs font-medium text-gray-600">Street Style</span>
                        <span class="px-3 py-1 border border-gray-200 rounded-full text-xs font-medium text-gray-600">Authentic</span>
                    </div>
                </div>
                <div class="lg:col-span-8">
                    <div class="aspect-[16/9] bg-gray-100 rounded-lg overflow-hidden relative group-hover:scale-[1.02] transition-transform duration-500 ease-out">
                        <img src="/generated/image-urban-creative-in-brooklyn-wearing-authe-1765505543945-2.webp" alt="Urban fashion workwear style" class="w-full h-full object-cover" />
                    </div>
                </div>
            </div>

            <!-- Collection 3: Heritage -->
            <div class="group grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <div class="lg:col-span-4 space-y-6">
                    <h3 class="font-serif text-3xl md:text-4xl text-gray-900">Heritage Since 1889</h3>
                    <p class="text-gray-600 text-lg leading-relaxed">
                        Over a century of authentic workwear craftsmanship. Our designs honor the original patterns and construction methods that built America.
                    </p>
                    <div class="flex flex-wrap gap-2 pt-2">
                        <span class="px-3 py-1 border border-gray-200 rounded-full text-xs font-medium text-gray-600">Original Designs</span>
                        <span class="px-3 py-1 border border-gray-200 rounded-full text-xs font-medium text-gray-600">Timeless</span>
                        <span class="px-3 py-1 border border-gray-200 rounded-full text-xs font-medium text-gray-600">Authentic</span>
                    </div>
                </div>
                <div class="lg:col-span-8">
                    <div class="aspect-[16/9] bg-gray-800 rounded-lg overflow-hidden relative group-hover:scale-[1.02] transition-transform duration-500 ease-out">
                        <img src="/generated/image-vintage-workwear-from-1930s-heritage-bra-1765505547076-3.webp" alt="Vintage Carhartt heritage workwear" class="w-full h-full object-cover" />
                    </div>
                </div>
            </div>

            <!-- Collection 4: Authenticity -->
            <div class="group grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <div class="lg:col-span-4 space-y-6">
                    <h3 class="font-serif text-3xl md:text-4xl text-gray-900">The Real Deal</h3>
                    <p class="text-gray-600 text-lg leading-relaxed">
                        Construction workers and fashion-forward creatives wearing the same gear. That's authentic workwear credibility you can't fake.
                    </p>
                    <div class="flex flex-wrap gap-2 pt-2">
                        <span class="px-3 py-1 border border-gray-200 rounded-full text-xs font-medium text-gray-600">Genuine</span>
                        <span class="px-3 py-1 border border-gray-200 rounded-full text-xs font-medium text-gray-600">Trusted</span>
                    </div>
                </div>
                <div class="lg:col-span-8">
                    <div class="aspect-[16/9] bg-gray-950 rounded-lg overflow-hidden relative group-hover:scale-[1.02] transition-transform duration-500 ease-out">
                        <img src="/generated/image-real-construction-worker-and-fashion-for-1765505550438-4.webp" alt="Workers and fashion buyers in Carhartt" class="w-full h-full object-cover" />
                    </div>
                </div>
            </div>
        </div>
        
        <div class="mt-12 md:hidden">
            <a href="/collections" class="flex items-center text-gray-500 hover:text-gray-900 transition-colors">
                View all <span class="ml-2">→</span>
            </a>
        </div>
    </section>

    <!-- Values Section -->
    <section class="bg-gray-50 px-6 md:px-12 lg:px-24 py-12 md:py-24" id="heritage">
        <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl text-gray-900 mb-16 max-w-3xl">Built on values that stand the test of time</h2>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <!-- Durability -->
            <div class="bg-white p-8 rounded-xl shadow-sm hover:shadow-md transition-shadow duration-300 flex flex-col h-full min-h-[400px]">
                <h3 class="text-xl font-semibold mb-4">Durability</h3>
                <p class="text-gray-600 text-sm leading-relaxed mb-auto">
                    Every piece is engineered to withstand the harshest conditions. We don't just make clothes—we build gear that lasts generations.
                </p>
                <div class="mt-8 flex justify-center h-48 items-end">
                    <img src="/generated/image-workwear-details---reinforced-pockets-he-1765505553783-5.webp" alt="Durable construction details" class="h-full w-full object-cover rounded-lg" />
                </div>
            </div>

            <!-- Authenticity -->
            <div class="bg-white p-8 rounded-xl shadow-sm hover:shadow-md transition-shadow duration-300 flex flex-col h-full min-h-[400px]">
                <h3 class="text-xl font-semibold mb-4">Authenticity</h3>
                <p class="text-gray-600 text-sm leading-relaxed mb-auto">
                    Real workwear for real people. From construction sites to city streets, our heritage speaks for itself.
                </p>
                <div class="mt-8 flex justify-center h-48 items-end">
                    <div class="h-full w-full bg-primary-900 rounded-lg flex items-center justify-center">
                        <span class="text-white font-bold text-4xl">1889</span>
                    </div>
                </div>
            </div>

            <!-- Craftsmanship -->
            <div class="bg-white p-8 rounded-xl shadow-sm hover:shadow-md transition-shadow duration-300 flex flex-col h-full min-h-[400px]">
                <h3 class="text-xl font-semibold mb-4">Craftsmanship</h3>
                <p class="text-gray-600 text-sm leading-relaxed mb-auto">
                    Triple-stitched seams, reinforced stress points, premium materials. Quality construction is our signature.
                </p>
                <div class="mt-8 flex justify-center h-48 items-end">
                    <div class="h-full w-full bg-gray-900 rounded-lg flex items-center justify-center p-8">
                        <svg class="w-24 h-24 text-primary-500" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M10.1214 2.40967C11.0087 2.40967 11.7683 3.04566 11.9242 3.91908L12.1482 5.17341C12.3042 6.04681 13.0638 6.68282 13.951 6.68282H15.47C17.83 6.68282 19.7432 8.59595 19.7432 10.9559C19.7432 12.3696 19.0567 13.6229 17.999 14.4007C18.4424 14.5514 18.7925 14.7906 19.0496 15.1048C19.3141 15.4514 19.5031 15.9439 19.6165 16.5641C19.6354 16.7283 19.6591 16.8879 19.6827 17.0475C19.7063 17.2071 19.7299 17.3667 19.7488 17.5309C19.7685 17.7014 19.783 17.8473 19.7951 17.9686C19.8062 18.0809 19.8153 18.1721 19.8244 18.2423C19.8622 18.7531 19.9189 19.1726 19.9945 19.4827C20.0742 19.9188 20.2352 20.3438 20.4633 20.7231H17.2352C17.084 20.4313 16.9895 20.0847 16.9139 19.7016C16.8489 19.3722 16.7979 18.9617 16.7368 18.4704C16.7268 18.3904 16.7166 18.3083 16.706 18.2241L16.5926 17.385C16.4981 16.7465 16.3847 16.2905 16.2713 15.9986C16.139 15.725 15.9312 15.5244 15.6476 15.4149C15.3453 15.3055 14.8917 15.2291 14.2491 15.2291H14.1037C13.2164 15.2291 12.4568 14.5931 12.3009 13.7197L12.0769 12.4653C11.9209 11.5919 11.1613 10.9559 10.274 10.9559H7.53417V15.8395H4.48193V2.40967H10.1214ZM16.6909 10.9559C16.6909 11.6302 16.1443 12.1769 15.47 12.1769H13.951C13.0638 12.1769 12.3042 11.5408 12.1482 10.6674L11.9242 9.41312C11.7683 8.53971 11.0087 7.9037 10.1214 7.9037H7.53417V5.46189H10.274C11.1613 5.46189 11.9209 6.0979 12.0769 6.97131L12.3008 8.22563C12.4568 9.09904 13.2164 9.73505 14.1037 9.73505H15.47C16.1443 9.73505 16.6909 10.2817 16.6909 10.9559Z" fill="currentColor"/>
                        </svg>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Stories Section -->
    <section class="bg-white px-6 md:px-12 lg:px-24 py-12 md:py-24" id="stories">
        <div class="flex flex-col md:flex-row justify-between items-end mb-12">
            <h2 class="font-serif text-3xl md:text-4xl text-gray-900">Stories from the field and the street</h2>
            <a href="/stories" class="hidden md:inline-flex items-center text-gray-500 hover:text-gray-900 transition-colors mt-4 md:mt-0">
                Read all <span class="ml-2">→</span>
            </a>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Story 1 -->
            <div class="group cursor-pointer">
                <div class="aspect-square bg-gray-900 rounded-lg overflow-hidden mb-4 relative">
                     <img src="/generated/image-construction-worker-in-rugged-workwear-o-1765505536451-0.webp" alt="Construction worker" class="w-full h-full object-cover" />
                     <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
                     <div class="absolute bottom-4 left-4 text-white font-bold text-lg">Built for the Job</div>
                </div>
                <h3 class="text-sm font-medium text-gray-900 group-hover:underline">How NYC Construction Workers Choose Their Gear</h3>
            </div>

             <!-- Story 2 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-primary-600 rounded-lg overflow-hidden mb-4 relative">
                    <img src="/generated/image-urban-creative-in-brooklyn-wearing-authe-1765505543945-2.webp" alt="Urban style" class="w-full h-full object-cover" />
                    <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
                    <div class="absolute bottom-4 left-4 text-white font-bold text-lg">Street Style</div>
                </div>
                <h3 class="text-sm font-medium text-gray-900 group-hover:underline">Brooklyn Creatives on Why They Choose Carhartt</h3>
            </div>

             <!-- Story 3 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-gray-800 rounded-lg overflow-hidden mb-4 relative">
                     <img src="/generated/image-vintage-workwear-from-1930s-heritage-bra-1765505547076-3.webp" alt="Heritage" class="w-full h-full object-cover" />
                     <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
                     <div class="absolute bottom-4 left-4 text-white font-bold text-lg">Heritage</div>
                </div>
                <h3 class="text-sm font-medium text-gray-900 group-hover:underline">135 Years of Authentic Workwear: The Carhartt Story</h3>
            </div>

             <!-- Story 4 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-gray-950 rounded-lg overflow-hidden mb-4 relative">
                    <img src="/generated/image-close-up-of-durable-workwear-jacket-with-1765505540718-1.webp" alt="Durability" class="w-full h-full object-cover" />
                    <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
                    <div class="absolute bottom-4 left-4 text-white font-bold text-lg">Quality</div>
                </div>
                <h3 class="text-sm font-medium text-gray-900 group-hover:underline">The Engineering Behind Our Triple-Stitched Construction</h3>
            </div>

             <!-- Story 5 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-primary-900 rounded-lg overflow-hidden mb-4 relative flex items-center justify-center">
                    <div class="text-center p-8">
                        <div class="text-white text-6xl font-bold mb-4">$89B</div>
                        <div class="text-white text-lg">Workwear Market</div>
                    </div>
                </div>
                <h3 class="text-sm font-medium text-gray-900 group-hover:underline">How Authentic Workwear Is Reshaping Urban Fashion</h3>
            </div>

             <!-- Story 6 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-gray-100 rounded-lg overflow-hidden mb-4 relative">
                     <img src="/generated/image-real-construction-worker-and-fashion-for-1765505550438-4.webp" alt="Authenticity" class="w-full h-full object-cover" />
                     <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
                     <div class="absolute bottom-4 left-4 text-white font-bold text-lg">Authenticity</div>
                </div>
                <h3 class="text-sm font-medium text-gray-900 group-hover:underline">Same Gear, Different Streets: Workers & Fashion Buyers Unite</h3>
            </div>
        </div>
    </section>

    <!-- Newsletter Section -->
    <section class="px-6 md:px-12 lg:px-24 py-12">
        <div class="bg-gradient-to-r from-primary-900 to-primary-800 rounded-2xl p-8 md:p-16 lg:p-20">
            <h3 class="font-serif text-2xl md:text-3xl text-white mb-4">Join the Carhartt Community</h3>
            <p class="text-primary-100 mb-8 max-w-md">Get exclusive access to new collections, heritage stories, and workwear insights delivered to your inbox.</p>
            
            <form class="flex flex-col sm:flex-row gap-4 max-w-lg">
                <input type="email" placeholder="your.email@example.com" class="flex-1 bg-white border-0 rounded-lg px-4 py-3 text-sm placeholder:text-gray-400 focus:ring-2 focus:ring-primary-500 outline-none" />
                <button type="submit" class="bg-white hover:bg-primary-50 transition-colors text-primary-900 px-6 py-3 rounded-lg text-sm font-semibold">
                    Subscribe
                </button>
            </form>
            <p class="text-[10px] text-primary-200 mt-4">We respect your privacy. By signing up, you agree to receive communications from Carhartt. Read our Privacy Policy.</p>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="relative bg-gradient-to-b from-gray-900 via-gray-800 to-gray-950 pt-32 pb-48 px-6 md:px-12 lg:px-24 overflow-hidden">
        <div class="absolute inset-0 opacity-10">
            <img src="/generated/image-construction-worker-in-rugged-workwear-o-1765505536451-0.webp" alt="Background" class="w-full h-full object-cover" />
        </div>
        <div class="max-w-5xl relative z-10">
            <h2 class="font-serif text-4xl md:text-6xl lg:text-7xl text-white leading-tight mb-8">
                Gear that works as hard as you do. <br />
                <span class="text-white/70">From the construction site to the city street, discover authentic workwear built to last since 1889.</span>
            </h2>
            
            <div class="mt-16 flex flex-wrap gap-4">
                 <a href="/collections" class="inline-flex items-center justify-center px-8 py-4 bg-primary-600 hover:bg-primary-700 rounded text-sm font-semibold text-white transition-colors duration-300">
                    Shop Collections
                </a>
                 <a href="/heritage" class="inline-flex items-center justify-center px-8 py-4 border border-white/30 rounded text-sm font-semibold text-white hover:bg-white hover:text-gray-900 transition-colors duration-300">
                    Our Heritage
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 text-gray-300 px-6 md:px-12 lg:px-24 pt-24 pb-12 relative overflow-hidden">
        <div class="relative z-10">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-24">
                <div class="col-span-1 md:col-span-2">
                    <div class="flex items-center gap-2 mb-6">
                        <svg class="w-10 h-10 text-primary-500" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M10.1214 2.40967C11.0087 2.40967 11.7683 3.04566 11.9242 3.91908L12.1482 5.17341C12.3042 6.04681 13.0638 6.68282 13.951 6.68282H15.47C17.83 6.68282 19.7432 8.59595 19.7432 10.9559C19.7432 12.3696 19.0567 13.6229 17.999 14.4007C18.4424 14.5514 18.7925 14.7906 19.0496 15.1048C19.3141 15.4514 19.5031 15.9439 19.6165 16.5641C19.6354 16.7283 19.6591 16.8879 19.6827 17.0475C19.7063 17.2071 19.7299 17.3667 19.7488 17.5309C19.7685 17.7014 19.783 17.8473 19.7951 17.9686C19.8062 18.0809 19.8153 18.1721 19.8244 18.2423C19.8622 18.7531 19.9189 19.1726 19.9945 19.4827C20.0742 19.9188 20.2352 20.3438 20.4633 20.7231H17.2352C17.084 20.4313 16.9895 20.0847 16.9139 19.7016C16.8489 19.3722 16.7979 18.9617 16.7368 18.4704C16.7268 18.3904 16.7166 18.3083 16.706 18.2241L16.5926 17.385C16.4981 16.7465 16.3847 16.2905 16.2713 15.9986C16.139 15.725 15.9312 15.5244 15.6476 15.4149C15.3453 15.3055 14.8917 15.2291 14.2491 15.2291H14.1037C13.2164 15.2291 12.4568 14.5931 12.3009 13.7197L12.0769 12.4653C11.9209 11.5919 11.1613 10.9559 10.274 10.9559H7.53417V15.8395H4.48193V2.40967H10.1214ZM16.6909 10.9559C16.6909 11.6302 16.1443 12.1769 15.47 12.1769H13.951C13.0638 12.1769 12.3042 11.5408 12.1482 10.6674L11.9242 9.41312C11.7683 8.53971 11.0087 7.9037 10.1214 7.9037H7.53417V5.46189H10.274C11.1613 5.46189 11.9209 6.0979 12.0769 6.97131L12.3008 8.22563C12.4568 9.09904 13.2164 9.73505 14.1037 9.73505H15.47C16.1443 9.73505 16.6909 10.2817 16.6909 10.9559Z" fill="currentColor"/>
                        </svg>
                        <span class="font-bold text-2xl text-white">Carhartt</span>
                    </div>
                    <p class="text-sm mb-6">Authentic workwear since 1889</p>
                    <a href="/contact" class="text-lg font-medium hover:text-white transition-colors inline-flex items-center">
                        Find a Store <span class="ml-2">→</span>
                    </a>
                </div>
                
                <div class="space-y-4">
                    <h4 class="font-semibold text-white">Shop</h4>
                    <div class="text-sm space-y-2">
                        <p><a href="/jackets" class="hover:text-white transition-colors">Jackets</a></p>
                        <p><a href="/pants" class="hover:text-white transition-colors">Pants</a></p>
                        <p><a href="/overalls" class="hover:text-white transition-colors">Overalls</a></p>
                        <p><a href="/accessories" class="hover:text-white transition-colors">Accessories</a></p>
                    </div>
                </div>

                <div class="space-y-4">
                    <h4 class="font-semibold text-white">Company</h4>
                    <div class="text-sm space-y-2">
                        <p><a href="/heritage" class="hover:text-white transition-colors">Our Heritage</a></p>
                        <p><a href="/stories" class="hover:text-white transition-colors">Stories</a></p>
                        <p><a href="/sustainability" class="hover:text-white transition-colors">Sustainability</a></p>
                        <p><a href="/careers" class="hover:text-white transition-colors">Careers</a></p>
                    </div>
                </div>
            </div>

            <div class="flex flex-col md:flex-row justify-between items-center border-t border-gray-800 pt-8">
                <div class="flex gap-6 text-sm font-medium mb-4 md:mb-0">
                    <a href="https://instagram.com/carhartt" class="hover:text-white transition-colors">Instagram</a>
                    <a href="https://facebook.com/carhartt" class="hover:text-white transition-colors">Facebook</a>
                    <a href="https://twitter.com/carhartt" class="hover:text-white transition-colors">Twitter</a>
                    <a href="https://youtube.com/carhartt" class="hover:text-white transition-colors">YouTube</a>
                </div>
                
                <div class="flex gap-6 text-xs">
                    <a href="/privacy" class="hover:text-white transition-colors">Privacy Policy</a>
                    <a href="/terms" class="hover:text-white transition-colors">Terms of Service</a>
                </div>
            </div>

            <div class="text-center text-xs opacity-50 mt-8">
                <p>© 2025 Carhartt. All rights reserved.</p>
            </div>
        </div>
    </footer>
</div>

<style>
    /* Custom utility for vertical writing mode */
    .writing-vertical-rl {
        writing-mode: vertical-rl;
    }
</style>

