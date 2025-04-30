<script>
    import { goto } from "$app/navigation";
    import AnsButton2 from "$lib/AnsButton2.svelte";
</script>

<div class="bg-black w-screen h-screen flex relative justify-center">
    <img id="scene2 -z-2" src={'/landing.png'} alt="" />
    <div class="absolute flex flex-col gap-8 mx-auto bottom-[30%]">
        <h1 class="text-center text-7xl text-[#040348]">BEAR POLAR</h1>
        <button class="bg-[#3e5879] text-white cursor-pointer px-9 py-3 rounded-full" onclick={() => {goto('story')}}>เริ่มต้น</button>
    </div>
</div>
