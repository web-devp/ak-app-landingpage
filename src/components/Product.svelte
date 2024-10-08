<script>
  import ProductCard from './ProductCard.svelte'
  import SectionWrapper from './SectionWrapper.svelte'
  let productFeatures = [
    {
      featureList: [
        'Driving talen towards a purpose with passion',
        'Dare to believe',
        'Putting Football first',
        '30x30m field for U-11'
      ],
      description:
        'Our qualified trainers ensures all players have the information they need to train safely and train effectively.',
      imgUrl: 'assets/dribbling.jpg'
    },

    {
      featureList: [
        'Nurturing footballers right from initiation to realizing their complete potential',
        'best in class facilities, coaches',
        'Focus on holistic development',
        'Inter-Academy matches'
      ],
      description:
        'Empowering athletes to be Champions, Leaders and Influencers.',
      imgUrl: 'assets/foot-on-ball.jpg'
    },
    {
      featureList: [
        'Driving talent towards a purpose with passion',
        'Dare to believe',
        'Putting Football first',
        '30x30m field for U-11'
      ],
      description:
        'Our qualified trainers ensures all players have the information they need to train safely and train effectively.',
      imgUrl: 'assets/skills.jpg'
    }
  ]
</script>

<SectionWrapper id="product">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Start your life <span class="text-indigo-400">Play Football</span>
        today
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Features For Everyone
      </h3>
    </div>
    {#each productFeatures as productFeature, index}
      <ProductCard {productFeature} {index}>
        {#if index === 0}
          Experience a beginner exercise <span
            class="text-indigo-400 font-medium">master</span
          > class
        {:else if index === 1}
          Lay the foundations for <span class="text-indigo-400 font-medium">
            routine
          </span> and consistency
        {:else}
          Workouts specific to your <span class="text-indigo-400 font-medium"
            >environment</span
          >
          and <span class="text-indigo-400 font-medium"> expertise</span>
        {/if}
      </ProductCard>
    {/each}
  </div>
</SectionWrapper>
