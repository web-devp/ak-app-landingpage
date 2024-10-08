<script>
  import SectionWrapper from './SectionWrapper.svelte'
  import ReviewCard from './ReviewCard.svelte'
  import Stars from './Stars.svelte'
  let lim = true
  let reviewsList = [
    {
      name: 'From a satisfied parent',
      review:
        "My son has been training at RFA for the past year, and we've seen a huge improvement in his skills. The coaches are incredibly knowledgeable and supportive, and the facilities are top-notch. I'm so grateful for the positive impact this academy has had on my son's development.",
      features: [
        'Experienced Coaches',
        'State-of-the-art facilities',
        'Goalkeeper Training Programme'
      ]
    },
    {
      name: 'From a Former Player',
      review:
        "I had the privilege of playing for RFA as a kid, and it was an experience I'll never forget. The coaches taught me not only about football but also about teamwork, discipline, and sportsmanship. I'm incredibly grateful for the foundation I received here, which helped me pursue my passion for the sport at a higher level",
      features: [
        'competitive environment',
        'strive for excellence',
        'tournament participation and scrimmages'
      ]
    },
    {
      name: 'From a Current Player',
      review:
        "I absolutely love training at RFA! The atmosphere is fun and competitive, and I'm constantly learning new things. The coaches push me to be my best, and I've made some great friends here.",
      features: [
        'state-of-the-art training equipment',
        'artificial turf fields',
        'Holistic Development'
      ]
    },
    {
      name: 'Alex Turner',
      review:
        'RFA has been a fantastic experience for my son. The coaches are knowledgeable and supportive, and the facilities are top-notch. My son has improved significantly in his skills and confidence since joining.',
      features: [
        'Experienced coaches',
        'Modern facilities',
        'Competitive atmosphere',
        'Friendly environment'
      ]
    },
    {
      name: 'Olivia Wilde',
      review:
        "I'm so impressed with RFA! My daughter has been having a blast training there. She loves the variety of drills and the team-building activities. The staff is always enthusiastic and encouraging.",
      features: [
        'Variety of training drills',
        'Team-building activities',
        'Supportive staff',
        'Fun atmosphere'
      ]
    },
    {
      name: 'Chris Hemsworth',
      review:
        'RFA is a great place for young athletes to develop their skills. The coaches are very focused on technique and provide personalized attention to each player. My son has made significant progress in a short time.',
      features: [
        'Personalized attention',
        'Focus on technique',
        'Competitive environment',
        'Quality coaching'
      ]
    }
  ]
</script>

<SectionWrapper>
  <div
    class="flex flex-col gap-10 sm:gap-14, md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Don't just take our word for it
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] max-auto w-full semi-bold text-center"
      >
        See What <span class="text-indigo-400">Others</span> Have To Say
      </h3>
    </div>
    <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} left={true} {index} />
        {/each}
      </div>
      <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} {index} />
        {/each}
      </div>
    </div>
    <button on:click={() => (lim = !lim)} class="specialBtn">
      <p>{lim ? 'Show More' : 'Show Less'}</p>
    </button>
    <div class="flex flex-col gap-10">
      <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
        Trusted by 1,349 Athletes
      </p>
      <Stars />
    </div>
  </div>
</SectionWrapper>
