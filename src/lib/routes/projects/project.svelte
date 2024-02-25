<script lang="ts">
    export let title:string;
    export let src:string = '';
    export let href:string = '';
</script>

<a class="project" href={href?`/#${href}`:null}>
    <div class="title">
        {title}
    </div>
    <div class="img-container" style={src? `background-image:url('${src}')` : ``}/>
</a>

<style>
    .project{
        box-sizing: border-box;

        width:300px;
        height:260px;

        border:5px solid white;
        border-radius: 10px;

        cursor: pointer;

        color:white;
        text-decoration: none;
    }

    .title{
        width:100%;
        height:40px;

        display:flex;
        justify-content: center;
        align-items: center;

        font-size: 26px;
        font-weight: bold;
    }

    .img-container{
        width:100%;
        height:calc(100% - 40px);

        background-size:contain;
        background-repeat: no-repeat;
        background-position: center;
    }

    .project:hover{
        border: 5px solid #00f9ff;
        box-shadow: 0 0 20px #57fcff;
    }
</style>