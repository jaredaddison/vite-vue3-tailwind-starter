<template>
  <div class="bg-gray-900">
    <div class="mx-auto max-w-7xl py-16 px-4 sm:py-24 sm:px-6 lg:px-8">
      <div class="lg:mx-auto lg:text-center lg:max-w-2xl">
        <h2 class="font-extrabold text-white tracking-tight text-3xl sm:text-4xl">
          The Current Plan
        </h2>
        <p class="mt-4 text-gray-400">Our current thoughts on the house and the plan from here</p>
      </div>
      <div class="mt-20">
        <dl class="space-y-10 lg:space-y-0 lg:grid lg:gap-x-8 lg:gap-y-10 lg:grid-cols-2">
          <div v-for="faq in faqs" :key="faq.id">
            <dt class="font-semibold text-white">
              {{ faq.question }}
            </dt>
            <dd class="mt-3 text-gray-400">
              {{ faq.answer }}
            </dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
const faqs = [
  {
    id: 1,
    question: "What are they currently asking?",
    answer:
      "The are asking $1.5million however there has been very little interest as far as we can tell, the property has been on for over a month and there are no offers on the table. The house is sitting idle and unoccupied and the seller is motivated to sell",
  },
  { id: 2,
    question: "What are the negatives?",
    answer: "The house is not 100% finished and needs likely $100-200k to finish it off properly. This includes air conditioning, loft area for Bailey, potential lift installation, kitchen in the underground area etc",
  },
  {
    id: 3,
    question: "What is the vision?",
    answer: "There are currently 2, if not 3 levels that would be able to be rented our as AirBNB, self contained suits. This would give us 2 or 3 revenue streams at $150-300 per room, per night. Conservative estimate would say $150 per night, 5 nights per fortnight and even at that we would be looking at an additional $60k per year revenue.",
  },
  {
    id: 4,
    question: "Who would buy the house?",
    answer: "The Addison Family Trust would likely hold the house as an asset for tax purposes with the Addison Family Investments / Jared provicding a personal guarantee for the loan",
  },
  {
    id: 5,
    question: "What are we going to offer and how do we see it going?",
    answer: "Looking at offering $1.25million with an excoected counter-offer of $1.4million. Hoping for $1.35million or as close to that as possible. This would leave us with a $500,000 mortgage and $200,000 in excess.",
  },
  {
    id: 6,
    question: "Are you excited?",
    answer: "Very very excited!!!"
  },
]
</script>