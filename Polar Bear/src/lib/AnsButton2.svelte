<script>
    import { goto } from "$app/navigation";

    let {
        isClick = $bindable(false),
        count = $bindable(0),
        btn1,
        btn2,
        ans,
        point = $bindable(0),
        specify_count_btn1 = $bindable(0),
        specify_count_btn2 = $bindable(0),
    } = $props();
</script>

<button
    onclick={() => {
        isClick = true;
        if(!specify_count_btn1) {
            count += 1;
        } else {
            count = specify_count_btn1
        }
        if (btn1 == ans) {
            point += 1;
        }
    }}
>
    <div
        class="text-gray-700 flex items-center justify-center w-[181px] h-[97px] bg-white mr-[1rem] rounded-2xl shadow-2xl transition-all duration-300 hover:bg-gray-50 hover:scale-106 cursor-pointer"
    >
        <h2>{btn1}</h2>
    </div>
</button>
<button
    onclick={() => {
        isClick = true;
        if(!specify_count_btn2) {
            count += 1;
        } else {
           
            count = specify_count_btn2
        }

        if (btn2 == ans) {
            point += 1;
            console.log(btn1, ans)
        }
    }}
>
    <div
        class="text-gray-700 flex items-center justify-center w-[181px] h-[97px] bg-white rounded-2xl shadow-2xl transition-all duration-300 hover:bg-gray-50 hover:scale-106 cursor-pointer"
    >
        <h2>{btn2}</h2>
    </div>
</button>
