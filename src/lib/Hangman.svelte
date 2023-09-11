<script lang="ts">
export let errors: number
</script>

<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 300 300" shape-rendering="geometricPrecision" text-rendering="geometricPrecision" class="text-stone-600">
    <g transform="translate(0 0.000001)">
        <line x1="-54.067711" y1="0" x2="145.932289" y2="0" transform="translate(94.067711 280)" fill="none" stroke="currentColor" stroke-width="4" stroke-linecap="round"/>
        <line x1="0" y1="112.37999" x2="0" y2="-127.62001" transform="translate(80 167.620009)" fill="none" stroke="currentColor" stroke-width="4"/>
        <line x1="-30" y1="2.248611" x2="15" y2="-27.751389" transform="translate(110 67.75139)" fill="none" stroke="currentColor" stroke-width="4"/>
        <line x1="-1.956543" y1="-17.897927" x2="-3.956543" y2="22.102073" transform="translate(191.956543 57.897927)" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
        <line x1="-67.205659" y1="0" x2="52.794341" y2="0" transform="translate(137.205659 40)" fill="none" stroke="currentColor" stroke-width="4" stroke-linecap="round"/>
    </g>
    <g transform="matrix(1.219869 0 0 1.219869-38.285699-49.445418)">
        <g>
            {#if errors >= 6}
                <line class="animated" x1="-10.939364" y1="-11.116726" x2="14.060636" y2="13.883274" transform="translate(196.939363 201.116725)" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round"/>
            {/if}
            {#if errors >= 5}
                <line class="animated" x1="14.704396" y1="-11.116726" x2="-10.295604" y2="13.883274" transform="translate(171.295603 201.116725)" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round"/>
            {/if}
        </g>
        <g>
            {#if errors >= 4}
                <line class="animated" x1="-12.443153" y1="0" x2="12.556847" y2="0" transform="translate(197.443152 160)" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round"/>
            {/if}
            {#if errors >= 3}
                <line class="animated" x1="12.683173" y1="0" x2="-12.316827" y2="0" transform="translate(172.316826 160)" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round"/>
            {/if}
        </g>
        {#if errors >= 2}
            <line class="animated" x1="0" y1="-27.160182" x2="0" y2="27.160182" transform="translate(186.003032 165.361293)" fill="none" stroke="currentColor" stroke-width="3"/>
        {/if}
        {#if errors >= 1}
            <ellipse class="animated" rx="16.043456" ry="16.043456" transform="matrix(0-1 1 0 186.003032 122.157655)" fill="none" stroke="currentColor" stroke-width="3"/>
        {/if}
    </g>
</svg>

<style>
.animated {
  stroke-dasharray: 100%;
  animation: dashed 2s linear;
}

@keyframes dashed {
  from {
    stroke-dashoffset: 100%;
  }
  
  to {
    stroke-dashoffset: 0;
  }
}
</style>
