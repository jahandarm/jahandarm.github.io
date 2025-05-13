<script>
    import * as config from '$lib/config'
    import Avatar from '$lib/assets/avatar.jpeg';
    import {Film, Music, SquareLibrary} from 'lucide-svelte';
</script>

<svelte:head>
    <title>{config.title}</title>
</svelte:head>

<div class="card rounded-box shadow-md text-lg flex flex-col md:flex-row items-center mx-2 p-2">
    <div class="avatar m-6">
        <div class="w-36 rounded-full">
            <img src={Avatar}/>
        </div>
    </div>
    <div class="flex flex-col prose w-full">
        <p class="font-bold">Jahandar Musayev</p>
        <p>Living since ‘96. Coding since ‘10.</p>
        <br/>
        <p>Senior Software Engineer at <a class="link" href="https://ryftpay.com/">RyftPay</a></p>
        <p>
            Software Engineer at <a class="link" href="https://www.manchester.ac.uk/"
        >University of Manchester</a
        >
        </p>
        <p>
            Alumnus of <a class="link" href="https://www.manchester.ac.uk/">University of Manchester</a>
        </p>
    </div>
    <div class="divider"></div>
    <div class="flex flex-col w-full space-y-2 my-2 mt-4 md:mt-0">
        <a class="rounded-box bg-base-200 border-2 hover:bg-accent p-2 flex w-full"
           href="https://www.goodreads.com/review/list/34603517-jahandar-musayev?page=1&shelf=read" target="_blank">
            <SquareLibrary class="mx-2"/>
            What I am reading
        </a>
        <a class="rounded-box bg-base-200 border-2 hover:bg-accent p-2 flex w-full"
           href="https://www.imdb.com/user/ur54617010/ratings/?ref_=ext_shr_lnk" target="_blank">
            <Film class="mx-2"/>
            What I am watching
        </a>
        <a class="rounded-box bg-base-200 border-2 hover:bg-accent p-2 flex w-full"
           href="https://music.apple.com/gb/playlist/favorite-songs/pl.u-ovU3MzYrd" target="_blank">
            <Music class="mx-2"/>
            What I am listening
        </a>
    </div>
</div>

