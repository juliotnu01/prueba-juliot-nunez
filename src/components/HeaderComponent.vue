<script setup>
import logo from '../assets/logo.svg'

const headerJul = ` w-full h-full grid grid-cols-12  px-6 py-1   bg-[#24292E] tex-white max-[640px]:grid-cols-4`
const inputSearch = ` ml-[13px] h-full  w-[85vh]   bg-transparent  text-[#B9B9B9]  focus:outline-none focus:ring-0 `
const hamburgerLogo = `flex gap-4 col-span-2 items-center`
const cursorInputSearch = `h-4 w-[0.125rem] absolute top-[-0.8rem] translate-y-[1.26rem] left-[0.7rem] bg-[#13B497] `
const SvgInputSearch = ` absolute top-[-1rem] translate-y-[1.26rem] right-[0.9rem]`
const wraperInputSearche = `w-full relative bg-[#1C2126] rounded-[6px] h-[30px] self-center before:content-[''] before:absolute  before:left-2 before:w-[1px] before:h-[70%] before:bg-[#13B497] before:top-[50%] before:translate-y-[-50%]`
const btnConfig = `bg-[#13B497] p-[8px] rounded-md`
const btnNotificacion = `bg-[#2F363D] p-2 rounded-lg relative `
const dotNotificacion = `w-3 h-3 bg-[#D9B75F] rounded-3xl absolute -top-[2px] -right-[2px]`
const btnMessage = `bg-[#2F363D] p-2 rounded-lg relative max-[640px]:hidden`
const dotMessage = `w-3 h-3 bg-[#D9B75F] rounded-3xl absolute -top-[2px] -right-[2px]`
const btngift = `bg-[#2F363D] p-2 rounded-lg relative max-[640px]:hidden`
const dotgift = `w-3 h-3 bg-[#647280] rounded-3xl absolute -top-[2px] -right-[2px]`
const NotificationSection = `flex gap-4  col-span-2 justify-end items-center max-[640px]:col-span-1 `
const SearchSection = `flex col-span-6  items-center gap-2 max-[640px]:hidden`
const UserSection = `flex gap-4 col-span-2 justify-end items-center max-[640px]:col-span-1 `
const WraperUserSection = `flex gap-2 bg-[#EEFFF30A] rounded-lg`
const UserAvatar = `w-10 h-10 bg-[#D3D6E4] rounded-lg `

</script>
<template>
    <div :class="headerJul">
        <div :class="hamburgerLogo">
            <svg width="26px" height="26px" viewBox="0 0 24 24">
                <path d="M4 18L20 18" stroke="#ffffff" stroke-width="2" stroke-linecap="round" />
                <path d="M4 12L20 12" stroke="#ffffff" stroke-width="2" stroke-linecap="round" />
                <path d="M4 6L20 6" stroke="#ffffff" stroke-width="2" stroke-linecap="round" />
            </svg>
            <img class="w-[46px] h-[46px]" :src="logo" />
        </div>
        <div :class="SearchSection">
            <div :class="wraperInputSearche">
                <input type="text" :class="inputSearch" id="inputSearch" placeholder="Search here" />
                <svg width="20px" height="20px" viewBox="0 0 24 24" fill="none" :class="SvgInputSearch">
                    <path
                        d="M15 15L21 21M10 17C6.13401 17 3 13.866 3 10C3 6.13401 6.13401 3 10 3C13.866 3 17 6.13401 17 10C17 13.866 13.866 17 10 17Z"
                        stroke="#A4A4A4" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                </svg>
            </div>
            <button :class="btnConfig">
                <svg width="10px" height="10px" viewBox="0 0 28 28" fill="none">
                    <path clip-rule="evenodd"
                        d="M14 20C17.3137 20 20 17.3137 20 14C20 10.6863 17.3137 8 14 8C10.6863 8 8 10.6863 8 14C8 17.3137 10.6863 20 14 20ZM18 14C18 16.2091 16.2091 18 14 18C11.7909 18 10 16.2091 10 14C10 11.7909 11.7909 10 14 10C16.2091 10 18 11.7909 18 14Z"
                        fill="#fff" fill-rule="evenodd" />
                    <path clip-rule="evenodd"
                        d="M0 12.9996V14.9996C0 16.5478 1.17261 17.822 2.67809 17.9826C2.80588 18.3459 2.95062 18.7011 3.11133 19.0473C2.12484 20.226 2.18536 21.984 3.29291 23.0916L4.70712 24.5058C5.78946 25.5881 7.49305 25.6706 8.67003 24.7531C9.1044 24.9688 9.55383 25.159 10.0163 25.3218C10.1769 26.8273 11.4511 28 12.9993 28H14.9993C16.5471 28 17.8211 26.8279 17.9821 25.3228C18.4024 25.175 18.8119 25.0046 19.2091 24.8129C20.3823 25.6664 22.0344 25.564 23.0926 24.5058L24.5068 23.0916C25.565 22.0334 25.6674 20.3813 24.814 19.2081C25.0054 18.8113 25.1757 18.4023 25.3234 17.9824C26.8282 17.8211 28 16.5472 28 14.9996V12.9996C28 11.452 26.8282 10.1782 25.3234 10.0169C25.1605 9.55375 24.9701 9.10374 24.7541 8.66883C25.6708 7.49189 25.5882 5.78888 24.5061 4.70681L23.0919 3.29259C21.9846 2.18531 20.2271 2.12455 19.0485 3.1103C18.7017 2.94935 18.3459 2.80441 17.982 2.67647C17.8207 1.17177 16.5468 0 14.9993 0H12.9993C11.4514 0 10.1773 1.17231 10.0164 2.6775C9.60779 2.8213 9.20936 2.98653 8.82251 3.17181C7.64444 2.12251 5.83764 2.16276 4.70782 3.29259L3.2936 4.7068C2.16377 5.83664 2.12352 7.64345 3.17285 8.82152C2.98737 9.20877 2.82199 9.60763 2.67809 10.0167C1.17261 10.1773 0 11.4515 0 12.9996ZM15.9993 3C15.9993 2.44772 15.5516 2 14.9993 2H12.9993C12.447 2 11.9993 2.44772 11.9993 3V3.38269C11.9993 3.85823 11.6626 4.26276 11.2059 4.39542C10.4966 4.60148 9.81974 4.88401 9.18495 5.23348C8.76836 5.46282 8.24425 5.41481 7.90799 5.07855L7.53624 4.70681C7.14572 4.31628 6.51256 4.31628 6.12203 4.7068L4.70782 6.12102C4.31729 6.51154 4.31729 7.14471 4.70782 7.53523L5.07958 7.90699C5.41584 8.24325 5.46385 8.76736 5.23451 9.18395C4.88485 9.8191 4.6022 10.4963 4.39611 11.2061C4.2635 11.6629 3.85894 11.9996 3.38334 11.9996H3C2.44772 11.9996 2 12.4474 2 12.9996V14.9996C2 15.5519 2.44772 15.9996 3 15.9996H3.38334C3.85894 15.9996 4.26349 16.3364 4.39611 16.7931C4.58954 17.4594 4.85042 18.0969 5.17085 18.6979C5.39202 19.1127 5.34095 19.6293 5.00855 19.9617L4.70712 20.2632C4.3166 20.6537 4.3166 21.2868 4.70712 21.6774L6.12134 23.0916C6.51186 23.4821 7.14503 23.4821 7.53555 23.0916L7.77887 22.8483C8.11899 22.5081 8.65055 22.4633 9.06879 22.7008C9.73695 23.0804 10.4531 23.3852 11.2059 23.6039C11.6626 23.7365 11.9993 24.1411 11.9993 24.6166V25C11.9993 25.5523 12.447 26 12.9993 26H14.9993C15.5516 26 15.9993 25.5523 15.9993 25V24.6174C15.9993 24.1418 16.3361 23.7372 16.7929 23.6046C17.5032 23.3985 18.1809 23.1157 18.8164 22.7658C19.233 22.5365 19.7571 22.5845 20.0934 22.9208L20.2642 23.0916C20.6547 23.4821 21.2879 23.4821 21.6784 23.0916L23.0926 21.6774C23.4831 21.2868 23.4831 20.6537 23.0926 20.2632L22.9218 20.0924C22.5855 19.7561 22.5375 19.232 22.7669 18.8154C23.1166 18.1802 23.3992 17.503 23.6053 16.7931C23.7379 16.3364 24.1425 15.9996 24.6181 15.9996H25C25.5523 15.9996 26 15.5519 26 14.9996V12.9996C26 12.4474 25.5523 11.9996 25 11.9996H24.6181C24.1425 11.9996 23.7379 11.6629 23.6053 11.2061C23.3866 10.4529 23.0817 9.73627 22.7019 9.06773C22.4643 8.64949 22.5092 8.11793 22.8493 7.77781L23.0919 7.53523C23.4824 7.14471 23.4824 6.51154 23.0919 6.12102L21.6777 4.7068C21.2872 4.31628 20.654 4.31628 20.2635 4.7068L19.9628 5.00748C19.6304 5.33988 19.1137 5.39096 18.6989 5.16979C18.0976 4.84915 17.4596 4.58815 16.7929 4.39467C16.3361 4.2621 15.9993 3.85752 15.9993 3.38187V3Z"
                        fill="#fff" fill-rule="evenodd" />
                </svg>
            </button>
        </div>
        <div :class="NotificationSection">
            <button :class="btnNotificacion">
                <svg width="26px" height="26px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                        d="M20.53 16.25C20.44 16.25 18.42 15.89 18.42 10C18.42 5.84 16 3.25 12 3.25C8 3.25 5.58 5.84 5.58 10C5.58 16 3.49 16.25 3.5 16.25C3.30109 16.25 3.11032 16.329 2.96967 16.4697C2.82902 16.6103 2.75 16.8011 2.75 17C2.75 17.1989 2.82902 17.3897 2.96967 17.5303C3.11032 17.671 3.30109 17.75 3.5 17.75H8.33C8.49694 18.6007 8.95423 19.367 9.62366 19.9178C10.2931 20.4686 11.1331 20.7698 12 20.7698C12.8669 20.7698 13.7069 20.4686 14.3763 19.9178C15.0458 19.367 15.5031 18.6007 15.67 17.75H20.51C20.7089 17.75 20.8997 17.671 21.0403 17.5303C21.181 17.3897 21.26 17.1989 21.26 17C21.26 16.8011 21.181 16.6103 21.0403 16.4697C20.8997 16.329 20.7089 16.25 20.51 16.25H20.53ZM12 19.25C11.5363 19.2491 11.0843 19.1044 10.7064 18.8357C10.3284 18.567 10.0432 18.1877 9.89 17.75H14.11C13.9568 18.1877 13.6716 18.567 13.2936 18.8357C12.9157 19.1044 12.4637 19.2491 12 19.25ZM5.76 16.25C6.48 15.16 7.08 13.25 7.08 10C7.08 6.75 8.88 4.75 12 4.75C15.12 4.75 16.92 6.66 16.92 10C16.92 13.34 17.52 15.16 18.24 16.25H5.76Z"
                        fill="#13B497" />
                </svg>
                <div :class="dotNotificacion" />
            </button>
            <button :class="btnMessage">
                <svg width="26px" height="26px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M8 8H16M8 12H13M7 16V21L12 16H20V4H4V16H7Z" stroke="#13B497" stroke-width="1.5"
                        stroke-linecap="round" stroke-linejoin="round" />
                </svg>
                <div :class="dotMessage" />
            </button>
            <button :class="btngift">
                <svg fill="#8D98A4" width="26px" height="26px" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg">
                    <path
                        d="M15.5 6a1.25 1.25 0 0 0-1.25-1.25h-1.06a2.19 2.19 0 0 0 .23-1A2.22 2.22 0 0 0 11.2 1.5 3.78 3.78 0 0 0 8 3.07 3.78 3.78 0 0 0 4.8 1.5a2.22 2.22 0 0 0-2.22 2.22 2.19 2.19 0 0 0 .23 1H1.75A1.25 1.25 0 0 0 .5 6v2.5h1.25v4.79A1.25 1.25 0 0 0 3 14.5h10a1.25 1.25 0 0 0 1.25-1.25V8.46h1.25zm-4.3-3.25a1 1 0 0 1 0 2H8.68a2.36 2.36 0 0 1 2.52-2zm-6.4 0a2.36 2.36 0 0 1 2.52 2H4.8a1 1 0 0 1 0-1.95zM1.75 6h4.37v1.21H1.75zm4.37 7.29H3V8.46h3.12zm1.26 0V6h1.24v7.29zm5.62 0H9.88V8.46H13zm1.25-6H9.88V6h4.37z" />
                </svg>
                <div :class="dotgift" />
            </button>
        </div>
        <div :class="UserSection">
            <div :class="WraperUserSection">
                <div :class="UserAvatar" >
                    <svg class="w-10 h-10" viewBox="0 -8 72 72" fill="#D9D9D9">
                        <path class="cls-1" d="M12.54,52.05H59.46a2.11,2.11,0,0,0,1.6-.7A1.73,1.73,0,0,0,61.49,50,25.8,25.8,0,0,0,47.9,30.45a16.8,16.8,0,0,1-23.8,0A25.8,25.8,0,0,0,10.51,50a1.75,1.75,0,0,0,.43,1.38A2.11,2.11,0,0,0,12.54,52.05Z"/><path class="cls-1" d="M25.43,28.6c.27.29.56.56.85.82a14.52,14.52,0,0,0,19.43,0,11.1,11.1,0,0,0,.86-.82c.27-.29.54-.58.79-.89a14.6,14.6,0,1,0-22.72,0C24.89,28,25.16,28.31,25.43,28.6Z"/>
                    </svg>
                </div>
                <span class="self-center max-[640px]:hidden">Juliot</span>
                <svg fill="#fff" width="20px" height="20px" viewBox="0 0 24 24" class="self-center ">
                    <path
                        d="M17,8H7a1,1,0,0,0-.768,1.641l5,6a1,1,0,0,0,1.536,0l5-6A1,1,0,0,0,17,8Zm-5,5.438L9.135,10h5.73Z" />
                </svg>
            </div>
        </div>
    </div>
</template>