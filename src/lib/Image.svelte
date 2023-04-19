<script lang="ts">
  export let src: string;
  export let alt = "";

  const mediaUrl = "https://www.example.com";

  function media(path: string) {
    console.log(path);

    if (path.startsWith("http")) {
      return path;
    } else {
      return `${mediaUrl}${path}`;
    }
  }
</script>

<img src={media(src)} {alt} />
