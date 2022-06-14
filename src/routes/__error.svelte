<script context="module">
    export function load({ error, status }) {
        return {
            props: {
                message: error.message,
                status // same as status: status
            }
        };
    }
  </script>
  
  <script>
    import Error404 from '$lib/error404.svelte';

    export let status;
  </script>
  
  {#if status == 404}
    <Error404/>
  {:else}
  wtf
  {/if}