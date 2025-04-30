<script>
    import AnsButton2 from "$lib/AnsButton2.svelte";

    let Btn2 = $state(false);

    let point = $state(0);
    
    let sceens = $state([
        {
            scene: "https://img2.pic.in.th/pic/Bg-.png",
            text: "เช้าวันหนึ่งคุณกำลังทำกิจวัตรตอนเช้าก่อนไปทำงาน อย่างปกติเช่นเคย :",
            pass: true,
        },
        {
            scene: "https://img5.pic.in.th/file/secure-sv1/Ex-.png",
            text: "คุณกำลังจะออกจากบ้านและบังเอิญไปเห็นขยะในบ้านสิ่งที่คุณจะทำคือ :",
            btn1: "เก็บ",
            btn2: "เดินผ่าน",
            ans: "เก็บ",
        },
        {
            scene: "https://img5.pic.in.th/file/secure-sv1/Bg-.png",
            text: "หลังจากนั้น คุณดูนาฬิกาก็พบว่าต้องไปทำงานซะแล้ว คุณจะ :",
            btn1: "พกถุงผ้าก่อนออกจากบ้าน",
            btn2: "พกแก้วเก็บความเย็นก่อนออกจากบ้าน",
            ans: "0",
        },
        {
            scene: "https://img5.pic.in.th/file/secure-sv1/bg-office.png",
            text: "วันนี้อากาศหนาว หิมะปกคลุมไปทุกที่แต่สุดท้ายตอนนี้คุณเดินทางมาถึงที่ทำงานแล้ว !",
            pass: true,
        },
        {
            scene: "https://img5.pic.in.th/file/secure-sv1/bg-02176be5530c4f40.png",
            text: "ระหว่างทางเดินไปโต๊ะทำงาน คุณพบห้องที่ไม่มีคนอยู่แต่มีไฟเปิดทิ้งไว้ คุณจะ :",
            btn1: "เดินไปปิดไฟในห้องนั้น",
            btn2: "เดินผ่านไป",
            ans: "เดินไปปิดไฟในห้องนั้น",
        },
        {
            scene: "https://img2.pic.in.th/pic/bg-.png",
            text: "คุณได้เดินต่อไปยังโต๊ะทำงานแล้วพบกับกระดาษอยู่บนโต๊ะคุณจึงหยิบมันขึ้นมาอ่าน",
            pass: true,
            ans: "0",
        },
        {
            scene: "https://i.gifer.com/embedded/download/9ZMo.gif",
            pass: true,
            ans: "0"
        },
        {
            scene: "https://img2.pic.in.th/pic/213555-3E5879-D8C4B6-F5EFE7-1.png",
            text: "ไม่นะ ! คุณหลุดเข้ามาในแถบอาร์กติกตอนเหนือ !!",
            pass: true,
            ans: "0",
        },
        {
            scene: "https://img5.pic.in.th/file/secure-sv1/bg-bear.png",
            text: "คุณพบหมีขั้วโลกตัวหนึ่งติดอยู่บนธารน้ำแข็งเล็ก ๆ กำลังต้องการความช่วยเหลือ คุณจะ :",
            btn1: "ไม่สนใจและเดินหาทางออก",
            btn2: "หาทางช่วยหมีได้สำเร็จ",
            ans: "หาทางช่วยหมีได้สำเร็จ",
            specify_count_btn1: 9,
            specify_count_btn2: 10
        },
        {
            scene: "https://img2.pic.in.th/pic/bg-bad-ending.png",
            text: "คุณปล่อยให้หมีที่น่าสงสาร สูญพันธ์ เพราะนั่นคือหมีขั้วโลกตัวสุดท้ายของโลก",
            pass: true
        },
        {
            scene: "https://img5.pic.in.th/file/secure-sv1/bg--1.png",
            text: "คุณช่วยหมีได้สำเร็จ !แล้วได้กลับมาสู่ห้องทำงานของคุณ",
            ans: "0",
            pass: true
        },
        {
            scene: "https://img5.pic.in.th/file/secure-sv1/BearPolar.png",
            text: "คุณพบกระดาษใบเดิมที่มีเนื้อหาเปลี่ยนไปเหมือนกับว่าหมีตัวนั้นอยากส่งข้อความให้คุณ !!",
            pass: true,
            ans: "0",
        },
        {
            scene: "https://img2.pic.in.th/pic/good-end-100.png",
            ans: "0",
            pass: true
        },
        {
            scene: "https://img2.pic.in.th/pic/good-end-20.png",
            ans: "0",
            pass: true
        },
        
    ]);

    let count = $state(0);

    $effect(() => {
        
    })
</script>

<div class="bg-black w-screen h-screen flex justify-center">
    {#each sceens as item, index}
        {#if count == index}
            <img id="scene2" src={item.scene} class="relative" alt="" />
            {#if item.pass && index == 6}
                <button
                    class="absolute z-1 w-[70px] cursor-pointer top-[28rem]"
                    onclick={() => {
                        count += 1;
                    }}
                    ><img
                        src="https://img5.pic.in.th/file/secure-sv1/istockphoto-1453962208-640x640-removebg-preview.png"
                        alt=""
                    /></button
                >
            {/if}
            <!-- {#if count == 9}
                <button onclick={() => {goto('/')}} class="absolute z-[3000] flex gap-5 top-[32%] bg-[#71e5ab] border-2 border-white rounded-full px-6 py-2 text-white">กลับบ้าน <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-house-icon lucide-house"><path d="M15 21v-8a1 1 0 0 0-1-1h-4a1 1 0 0 0-1 1v8"/><path d="M3 10a2 2 0 0 1 .709-1.528l7-5.999a2 2 0 0 1 2.582 0l7 5.999A2 2 0 0 1 21 10v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/></svg></button>
            {/if} -->
            {#if item.pass && index == 7}
                <h1
                class="text-white absolute font-medium mt-[14rem] mb-[5rem] w-[400px] text-center text-2xl text-shadow-lg"
                >
                {item.text}
                </h1>
            {/if}
            {#if item.pass && index != 6 && index != 8 && index != 9 && index != 11 && index != 12}
                <button
                    class="absolute z-1 w-[200px] cursor-pointer top-[22rem]"
                    onclick={() => {
                        count += 1;
                    }}
                    ><img
                        src="https://img5.pic.in.th/file/secure-sv1/istockphoto-1453962208-640x640-removebg-preview.png"
                        alt=""
                    /></button
                >
            {/if}
            {#if item.pass && count == 11}
                <p class="absolute top-[350px] text-gray-500">
                    กรุณากดที่รูปหมี
                </p>
                <!-- svelte-ignore a11y_consider_explicit_label -->
                <button
                    onclick={() => {
                        count += 1;
                    }}
                    ><div
                        class="absolute left-[530px] z-20 w-[400px] h-[300px] cursor-pointer"
                    ></div></button
                >
            {/if}
            {#if item.pass && count == 5}
                <p class="absolute top-[300px] text-gray-500">
                    กรุณากดที่รูปหมี
                </p>
                <!-- svelte-ignore a11y_consider_explicit_label -->
                <button
                    onclick={() => {
                        count += 1;
                    }}
                    ><div
                        class="absolute left-[530px] z-20 w-[400px] h-[300px] cursor-pointer"
                    ></div></button
                >
            {/if}
            <h1
                class="text-black absolute font-medium mt-[14rem] mb-[5rem] w-[400px] text-center text-2xl text-shadow-lg"
            >
                {item.text}
            </h1>
            <div class="w-[430px] flex-col items-center flex h-screen absolute">
                {#if !item.pass}
                    <div class="flex mt-[21rem]">
                        <AnsButton2
                            bind:isClick={Btn2}
                            bind:count
                            btn1={item.btn1}
                            btn2={item.btn2}
                            specify_count_btn1={item.specify_count_btn1}
                            specify_count_btn2={item.specify_count_btn2}
                            ans={item.ans}
                            bind:point
                        />
                    </div>
                {/if}
            </div>
        {/if}
    {/each}
    <audio class="absolute opacity-5" controls autoplay loop>
        <source src="/Bright Horizon  Relaxing music.mp3">
    </audio>
</div>
