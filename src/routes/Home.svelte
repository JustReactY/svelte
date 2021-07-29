<script lang="ts">
    import { Link } from "svelte-routing";
    import logo from "../assets/svelte.png";

    interface ISPathsData {
        title: string;
        path: string;
    }

    const paths: Array<ISPathsData> = [
        {
            title: "丝滑的变量定义",
            path: "/data",
        },
        {
            title: "优秀的样式隔离",
            path: "/styles",
        },
        {
            title: "优雅的嵌套组件",
            path: "/mixin",
        },
        {
            title: "渲染富文本代码块",
            path: "/htmls",
        },
        {
            title: "傻瓜式的组件通信",
            path: "/props",
        },
    ];
</script>

<main>
    <img src={logo} alt="Svelte Logo" />
    <ul>
        {#each paths as path}
            <li>
                <Link to={path.path}>{path.title}</Link>
            </li>
        {/each}
    </ul>
</main>

<style>
    :root {
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
            Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
    }

    main {
        text-align: center;
        padding: 1em;
        margin: 0 auto;
    }

    img {
        height: 16rem;
        width: 16rem;
    }

    ul {
        margin: 0;
        padding: 0;
    }
    li {
        list-style-type: none;
    }

    @media (min-width: 480px) {
    }
</style>
