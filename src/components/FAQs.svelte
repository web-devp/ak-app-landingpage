<script>
  import SectionWrapper from './SectionWrapper.svelte'
  let faqs = [
    {
      question: 'What is the age range for your academy?',
      answer: 'Our academy is open to children ages 6-14.'
    },
    {
      question: 'What are the fees for the academy?',
      answer:
        'The fees vary depending on the age group and the frequency of training sessions. Please contact us for more information.'
    },
    {
      question: 'Do you offer competitive teams?',
      answer:
        'Yes, we offer competitive teams that participate in local and regional tournaments.'
    },
    {
      question: 'What are the qualifications of your coaches?',
      answer:
        'Our coaches are experienced and qualified soccer professionals with a passion for developing young talent.'
    },
    {
      question: 'What are the facilities like at the academy?',
      answer:
        'We have state-of-the-art facilities, including indoor and outdoor training fields, a fitness center, and a locker room.'
    },
    {
      question: 'What is the typical training schedule?',
      answer:
        'Training sessions are typically held five days a week, but the schedule may vary depending on the age group and team.'
    },
    {
      question:
        'Do you offer any additional programs, such as summer camps or clinics?',
      answer:
        'Yes, we offer a variety of additional programs throughout the year, including summer camps, clinics, and individual training sessions.'
    },
    {
      question: 'How can I register my child for the academy?',
      answer:
        'You can register your child online or by contacting us directly. We will be happy to answer any questions you may have.'
    }
  ]
</script>

<SectionWrapper id="faqs">
  <div
    class="flex flex-col gap-10 sm:gap-14, md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        For all your questions, qualms & querries
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] max-auto w-full semi-bold text-center"
      >
        Frequently <span class="text-indigo-400">Asked</span> Questions
      </h3>
    </div>
    <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
      {#each faqs as faq}
        <div
          class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
          ></div>
          <h4 class="text-lg sm:text-xl md:text-2xl pt-2">{faq.question}</h4>
          <p class="pl-2">{faq.answer}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrapper>
