<template>
  <main class="page page-index">
    <IndexHeader />
    <IndexProducts v-if="this.$store.state.index === 0"/>
    <ProductsMask v-if="this.$store.state.index === 1"/>
    <ProductsProtection v-if="this.$store.state.index === 2"/>
    <ProductsSanitazer v-if="this.$store.state.index === 3"/>
    <ProductsTest v-if="this.$store.state.index === 4"/>
    <ProductsDispenser v-if="this.$store.state.index === 5"/>
    <ProductsOther v-if="this.$store.state.index === 6"/>
    <IndexProtections />
    <IndexFaq />
    <IndexContact />
    <IndexFooter />
  </main>
</template>