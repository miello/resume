<script lang="ts">
  export let name: string = "Foo";
  export let nickname: string = "";
  export let phone: string = "";
  export let email: string = "";
  export let github: string = "";
  export let linkedin: string = "";
  export let location: string = "";
  export let website: string = "";
</script>

<div>
  <h2
    class="flex-none order-first sm:order-none print:order-none text-2xl sm:text-lg md:text-xl lg:text-3xl text-center p-4 pb-0 print:pt-0"
  >
    {name}
    <span class="block -mt-1 text-base lg:text-lg">({nickname})</span>
  </h2>
  <div
    class="flex flex-wrap flex-col print:text-xs sm:flex-row print:flex-row mb-2 text-sm sm:text-base"
  >
    <div class="flex-1 text-left w-48">
      <p><a href={`tel:${phone}`}>{phone}</a></p>
      <p><a href={`mailto:${email}`}>{email}</a></p>
      <p>{location}</p>
    </div>

    <div
      class="flex-1 text-left sm:text-right print:text-right print:text-xs w-48 mb-2 text-sm sm:text-base"
    >
      <p>
        <a
          href={`https://github.com/${github}`}
          target="_blank"
          rel="noreferrer">github.com/{github}</a
        >
      </p>
      <p>
        <a href={`https://${website}`} target="_blank" rel="noreferrer"
          >{website}</a
        >
      </p>
      {#if linkedin}
        <p>
          <a
            href={`https://linkedin.com/in/${linkedin}`}
            target="_blank"
            rel="noreferrer">linkedin.com/in/{linkedin}</a
          >
        </p>
      {/if}
    </div>
  </div>
</div>

<style>
  a {
    text-decoration: underline;
  }
</style>
