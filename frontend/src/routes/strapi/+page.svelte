<script>
  /** @type {import('./$types').PageData} */  export let data;
  console.log(data);
</script>

<h1>Hello Strapi</h1>
<h2>{data.attributes?.pricing?.title}</h2>
<span>{data.attributes?.pricing?.description}</span>
<img src={`http://localhost:1337${data.attributes?.pricing?.image?.data?.attributes?.url}`} style="max-width: 50%;" />

{#each data.attributes?.customers as customer}
<h2>{customer.title}</h2>
<span>{customer.description}</span>
{/each}