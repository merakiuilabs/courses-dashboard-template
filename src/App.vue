<template>
    <div class="relative min-h-screen lg:flex">
        <header class="text-gray-100 bg-gray-800 lg:hidden">
            <div class="container flex items-center justify-between p-4 mx-auto">
                <a href="#" class="text-white">
                    <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z" />
                    </svg>
                </a>
                
                <button @click="isOpen = !isOpen" class="p-2 text-white rounded-lg focus:outline-none hover:bg-gray-700">
                    <svg v-show="!isOpen" xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16m-7 6h7" />
                    </svg>
    
                    <svg v-show="isOpen" class="w-6 h-6 transition duration-200 ease-in-out" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>
            </div>
        </header>

        <div v-cloak :class="isOpen ? 'block' : 'hidden'" @click="isOpen = false" class="fixed inset-0 z-20 transition-opacity bg-black opacity-30 lg:hidden"></div>

        <aside id="sidebar" :class="isOpen ? 'translate-x-0 ease-in' : '-translate-x-full ease-out'" class="fixed inset-y-0 left-0 z-30 flex flex-col w-[4.5rem] min-h-screen space-y-6 overflow-y-auto text-gray-100 transition duration-200 transform bg-gray-800 lg:translate-x-0 lg:relative lg:inset-0">
            <div class="flex flex-col items-center flex-1 space-y-6">
                <a href="#" class="flex items-center justify-center w-full p-5 lg:p-0 lg:h-20 font-bold text-white truncate bg-blue-600 whitespace-nowrap">
                    <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z" />
                    </svg>
                </a>

                <nav class="flex flex-col items-center space-y-6">
                    <a href="#" class="p-2 transition-colors duration-300 rounded-lg group hover:bg-white">
                        <svg class="w-5 h-5 stroke-blue-100/50" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path class="group-hover:stroke-blue-700" d="M22 18.2222C22 18.6937 21.7893 19.1459 21.4142 19.4793C21.0391 19.8127 20.5304 20 20 20H4C3.46957 20 2.96086 19.8127 2.58579 19.4793C2.21071 19.1459 2 18.6937 2 18.2222V5.77778C2 5.30628 2.21071 4.8541 2.58579 4.5207C2.96086 4.1873 3.46957 4 4 4H9L11 6.66667H20C20.5304 6.66667 21.0391 6.85397 21.4142 7.18737C21.7893 7.52076 22 7.97295 22 8.44444V18.2222Z" fill="#969CBA" fill-opacity="0.2" stroke="#969CBA" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
                    </a>

                    <a href="#" class="p-3 transition-colors duration-300 bg-white rounded-lg">
                        <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 stroke-blue-700" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" />
                        </svg>
                    </a>

                    <a href="#" class="p-2 transition-colors duration-300 rounded-lg group hover:bg-white">
                        <svg class="w-5 h-5 group-hover:stroke-blue-700 " viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path class=" group-hover:stroke-blue-700" d="M4 4H20C21.1 4 22 4.9 22 6V18C22 19.1 21.1 20 20 20H4C2.9 20 2 19.1 2 18V6C2 4.9 2.9 4 4 4Z" fill="#969CBA" fill-opacity="0.2" stroke="#969CBA" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                            <path class=" group-hover:stroke-blue-700" d="M22 6L12 13L2 6" stroke="#969CBA" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
                    </a>

                    <a href="#" class="p-2 transition-colors duration-300 rounded-lg group hover:bg-white">
                        <svg class="w-5 h-5 group-hover:stroke-blue-700 " viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path class=" group-hover:stroke-blue-700" d="M13 2H6C5.46957 2 4.96086 2.21071 4.58579 2.58579C4.21071 2.96086 4 3.46957 4 4V20C4 20.5304 4.21071 21.0391 4.58579 21.4142C4.96086 21.7893 5.46957 22 6 22H18C18.5304 22 19.0391 21.7893 19.4142 21.4142C19.7893 21.0391 20 20.5304 20 20V9L13 2Z" fill="#969CBA" fill-opacity="0.2" stroke="#969CBA" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                            <path class=" group-hover:stroke-blue-700" d="M13 2V9H20" stroke="#969CBA" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
                    </a>
                </nav>
            </div>

            <div class="flex justify-center py-5 border-t border-gray-600">
                <a href="#" class="p-2 transition-colors duration-300 rounded-lg group hover:bg-white">
                    <svg class="w-5 h-5 opacity-100 group-hover:stroke-blue-700 " viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path class="group-hover:stroke-blue-700" d="M12 15C13.6569 15 15 13.6569 15 12C15 10.3431 13.6569 9 12 9C10.3431 9 9 10.3431 9 12C9 13.6569 10.3431 15 12 15Z" stroke="#969CBA" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        <path class="group-hover:stroke-blue-700" d="M19.4 15C19.2669 15.3016 19.2272 15.6362 19.286 15.9606C19.3448 16.285 19.4995 16.5843 19.73 16.82L19.79 16.88C19.976 17.0657 20.1235 17.2863 20.2241 17.5291C20.3248 17.7719 20.3766 18.0322 20.3766 18.295C20.3766 18.5578 20.3248 18.8181 20.2241 19.0609C20.1235 19.3037 19.976 19.5243 19.79 19.71C19.6043 19.896 19.3837 20.0435 19.1409 20.1441C18.8981 20.2448 18.6378 20.2966 18.375 20.2966C18.1122 20.2966 17.8519 20.2448 17.6091 20.1441C17.3663 20.0435 17.1457 19.896 16.96 19.71L16.9 19.65C16.6643 19.4195 16.365 19.2648 16.0406 19.206C15.7162 19.1472 15.3816 19.1869 15.08 19.32C14.7842 19.4468 14.532 19.6572 14.3543 19.9255C14.1766 20.1938 14.0813 20.5082 14.08 20.83V21C14.08 21.5304 13.8693 22.0391 13.4942 22.4142C13.1191 22.7893 12.6104 23 12.08 23C11.5496 23 11.0409 22.7893 10.6658 22.4142C10.2907 22.0391 10.08 21.5304 10.08 21V20.91C10.0723 20.579 9.96512 20.258 9.77251 19.9887C9.5799 19.7194 9.31074 19.5143 9 19.4C8.69838 19.2669 8.36381 19.2272 8.03941 19.286C7.71502 19.3448 7.41568 19.4995 7.18 19.73L7.12 19.79C6.93425 19.976 6.71368 20.1235 6.47088 20.2241C6.22808 20.3248 5.96783 20.3766 5.705 20.3766C5.44217 20.3766 5.18192 20.3248 4.93912 20.2241C4.69632 20.1235 4.47575 19.976 4.29 19.79C4.10405 19.6043 3.95653 19.3837 3.85588 19.1409C3.75523 18.8981 3.70343 18.6378 3.70343 18.375C3.70343 18.1122 3.75523 17.8519 3.85588 17.6091C3.95653 17.3663 4.10405 17.1457 4.29 16.96L4.35 16.9C4.58054 16.6643 4.73519 16.365 4.794 16.0406C4.85282 15.7162 4.81312 15.3816 4.68 15.08C4.55324 14.7842 4.34276 14.532 4.07447 14.3543C3.80618 14.1766 3.49179 14.0813 3.17 14.08H3C2.46957 14.08 1.96086 13.8693 1.58579 13.4942C1.21071 13.1191 1 12.6104 1 12.08C1 11.5496 1.21071 11.0409 1.58579 10.6658C1.96086 10.2907 2.46957 10.08 3 10.08H3.09C3.42099 10.0723 3.742 9.96512 4.0113 9.77251C4.28059 9.5799 4.48572 9.31074 4.6 9C4.73312 8.69838 4.77282 8.36381 4.714 8.03941C4.65519 7.71502 4.50054 7.41568 4.27 7.18L4.21 7.12C4.02405 6.93425 3.87653 6.71368 3.77588 6.47088C3.67523 6.22808 3.62343 5.96783 3.62343 5.705C3.62343 5.44217 3.67523 5.18192 3.77588 4.93912C3.87653 4.69632 4.02405 4.47575 4.21 4.29C4.39575 4.10405 4.61632 3.95653 4.85912 3.85588C5.10192 3.75523 5.36217 3.70343 5.625 3.70343C5.88783 3.70343 6.14808 3.75523 6.39088 3.85588C6.63368 3.95653 6.85425 4.10405 7.04 4.29L7.1 4.35C7.33568 4.58054 7.63502 4.73519 7.95941 4.794C8.28381 4.85282 8.61838 4.81312 8.92 4.68H9C9.29577 4.55324 9.54802 4.34276 9.72569 4.07447C9.90337 3.80618 9.99872 3.49179 10 3.17V3C10 2.46957 10.2107 1.96086 10.5858 1.58579C10.9609 1.21071 11.4696 1 12 1C12.5304 1 13.0391 1.21071 13.4142 1.58579C13.7893 1.96086 14 2.46957 14 3V3.09C14.0013 3.41179 14.0966 3.72618 14.2743 3.99447C14.452 4.26276 14.7042 4.47324 15 4.6C15.3016 4.73312 15.6362 4.77282 15.9606 4.714C16.285 4.65519 16.5843 4.50054 16.82 4.27L16.88 4.21C17.0657 4.02405 17.2863 3.87653 17.5291 3.77588C17.7719 3.67523 18.0322 3.62343 18.295 3.62343C18.5578 3.62343 18.8181 3.67523 19.0609 3.77588C19.3037 3.87653 19.5243 4.02405 19.71 4.21C19.896 4.39575 20.0435 4.61632 20.1441 4.85912C20.2448 5.10192 20.2966 5.36217 20.2966 5.625C20.2966 5.88783 20.2448 6.14808 20.1441 6.39088C20.0435 6.63368 19.896 6.85425 19.71 7.04L19.65 7.1C19.4195 7.33568 19.2648 7.63502 19.206 7.95941C19.1472 8.28381 19.1869 8.61838 19.32 8.92V9C19.4468 9.29577 19.6572 9.54802 19.9255 9.72569C20.1938 9.90337 20.5082 9.99872 20.83 10H21C21.5304 10 22.0391 10.2107 22.4142 10.5858C22.7893 10.9609 23 11.4696 23 12C23 12.5304 22.7893 13.0391 22.4142 13.4142C22.0391 13.7893 21.5304 14 21 14H20.91C20.5882 14.0013 20.2738 14.0966 20.0055 14.2743C19.7372 14.452 19.5268 14.7042 19.4 15V15Z" fill="#969CBA" fill-opacity="0.2" stroke="#969CBA" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                </a>
            </div>
        </aside>

        <main id="content" class="flex-1 pb-12 space-y-6 overflow-y-auto bg-gray-100 lg:h-screen md:space-y-8">
            <header class="flex items-center justify-between h-20 px-6 bg-white border-b">
                <div class="relative flex items-center">
                    <span class="absolute inset-y-0 left-0 flex items-center pl-3">
                        <svg class="w-5 h-5 text-gray-400" viewBox="0 0 24 24" fill="none">
                            <path d="M21 21L15 15M17 10C17 13.866 13.866 17 10 17C6.13401 17 3 13.866 3 10C3 6.13401 6.13401 3 10 3C13.866 3 17 6.13401 17 10Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path>
                        </svg>
                    </span>
                    
                    <input type="text" class="py-2.5 pl-10 pr-4 text-gray-700 placeholder-gray-400 bg-white border border-transparent border-gray-200 rounded-lg sm:w-auto w-36 focus:border-blue-400 focus:outline-none focus:ring focus:ring-blue-300 focus:ring-opacity-40" placeholder="Search">
                </div>

                <div class="flex items-center">
                    <div class="relative">
                        <button class="transition-colors duration-300 rounded-lg sm:px-4 sm:py-2 focus:outline-none hover:bg-gray-100" @click="dropdownOpen = !dropdownOpen">
                            <span class="sr-only">User Menu</span>
                            <div class="flex items-center md:-mx-2 ">
                                <div class="hidden md:mx-2 md:flex md:flex-col md:items-end md:leading-tight">
                                    <span class="font-semibold text-sm text-gray-800">Dhaiflaah</span>
                                    <span class="text-sm text-gray-600">Lecturer</span>
                                </div>
        
                                <img class="flex-shrink-0 w-10 h-10 overflow-hidden bg-gray-100 rounded-full md:mx-2" src="https://randomuser.me/api/portraits/men/68.jpg" alt="user profile photo" >
                            </div>
                        </button>
                        
                        <transition
                            enter-active-class="transition duration-200 ease-out"
                            enter-from-class="transform scale-95 opacity-0"
                            enter-to-class="transform scale-100 opacity-100"
                            leave-active-class="transition duration-75 ease-in"
                            leave-from-class="transform scale-100 opacity-100"
                            leave-to-class="transform scale-95 opacity-0"
                        >
                            <div class="absolute right-0 z-50 w-56 p-2 bg-white border rounded-lg top-16 lg:top-20" v-show="dropdownOpen">
                                <div class="px-4 py-2 text-gray-800 transition-colors duration-300 rounded-lg cursor-pointer hover:bg-gray-100">Profile</div>
                                <div class="px-4 py-2 text-gray-800 transition-colors duration-300 rounded-lg cursor-pointer hover:bg-gray-100">Messages</div>
                                <div class="px-4 py-2 text-gray-800 transition-colors duration-300 rounded-lg cursor-pointer hover:bg-gray-100">To-Do's</div>
                            </div>
                        </transition>
                    </div>

                    <div v-show="dropdownOpen" class="fixed inset-0 z-30" @click="dropdownOpen = false"></div>

                    <button class="relative p-2 mx-3 text-gray-400 transition-colors duration-300 rounded-full hover:bg-gray-100 hover:text-gray-600 focus:bg-gray-100">
                        <span class="sr-only">Notifications</span>
                        <span class="absolute top-0 right-0 w-2 h-2 mt-1 mr-2 bg-blue-700 rounded-full"></span>
                        <span class="absolute top-0 right-0 w-2 h-2 mt-1 mr-2 bg-blue-700 rounded-full animate-ping"></span>
                        
                        <svg aria-hidden="true" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9" />
                        </svg>
                    </button>

                    <button class="p-2 text-gray-400 transition-colors duration-300 rounded-full focus:outline-none hover:bg-gray-100 hover:text-gray-600 focus:bg-gray-100">
                        <span class="sr-only">Log out</span>
                        
                        <svg aria-hidden="true" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1" />
                        </svg>
                    </button>
                </div>
            </header>

            <section class="flex flex-col w-full px-6 md:justify-between md:items-center md:flex-row">
                <div>
                    <h2 class="text-3xl font-medium text-gray-800">Dashboard</h2>
                    <p class="mt-2 text-sm text-gray-500">Mobile UX/UI Design Course</p>
                </div>

                <div class="flex flex-col mt-6 md:flex-row md:-mx-1 md:mt-0">
                    <button class="px-6 py-3 focus:outline-none text-gray-500 transition-colors duration-300 rounded-lg md:mx-1 hover:bg-gray-400 hover:text-white">
                        <div class="flex items-center justify-center -mx-1">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 mx-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M11 5H6a2 2 0 00-2 2v11a2 2 0 002 2h11a2 2 0 002-2v-5m-1.414-9.414a2 2 0 112.828 2.828L11.828 15H9v-2.828l8.586-8.586z" />
                            </svg>
    
                            <span class="mx-1 text-sm capitalize">Manage dashboard</span>
                        </div>
                    </button>

                    <button class="px-6 py-3 focus:outline-none mt-4 text-white bg-blue-600 rounded-lg md:mt-0 md:mx-1 hover:bg-blue-500">
                        <div class="flex items-center justify-center -mx-1">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 mx-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M12 6v6m0 0v6m0-6h6m-6 0H6" />
                            </svg>
    
                            <span class="mx-1 text-sm capitalize">Create new course</span>
                        </div>
                    </button>
                </div>
            </section>

            <section class="grid grid-cols-1 gap-8 px-6 xl:grid-cols-3 2xl:grid-cols-4 md:grid-cols-2 ">
                <div class="flex items-center px-6 py-8 bg-white rounded-lg shadow-md shadow-gray-200 ">
                    <div class="flex items-center -mx-2">
                        <svg class="mx-2" width="70" height="70" viewBox="0 0 70 70" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="35" cy="35" r="35" fill="#713BDB" fill-opacity="0.05" />
                            <path d="M26 44C26 40.625 30.5 40.625 32.75 38.375C33.875 37.25 30.5 37.25 30.5 31.625C30.5 27.8754 31.9996 26 35 26C38.0004 26 39.5 27.8754 39.5 31.625C39.5 37.25 36.125 37.25 37.25 38.375C39.5 40.625 44 40.625 44 44" stroke="#6F52ED" stroke-width="2" stroke-linecap="square" />
                        </svg>
    
                        <div class="mx-2">
                            <h3 class="text-2xl font-medium text-gray-800">62</h3>
                            <p class="mt-1 text-sm text-gray-500">Students</p>
                        </div>
                    </div>
                </div>

                <div class="flex items-center px-6 py-8 bg-white rounded-lg shadow-md shadow-gray-200 ">
                    <div class="flex items-center -mx-2">
                        <svg class="mx-2" width="70" height="70" viewBox="0 0 70 70" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="35" cy="35" r="35" fill="#33D69F" fill-opacity="0.07" />
                            <path d="M26 39L31 34" stroke="#21B8C7" stroke-width="2" stroke-linecap="round"
                                stroke-linejoin="round" />
                            <path
                                d="M32 34C32.5523 34 33 33.5523 33 33C33 32.4477 32.5523 32 32 32C31.4477 32 31 32.4477 31 33C31 33.5523 31.4477 34 32 34Z"
                                stroke="#21B8C7" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                            <path
                                d="M37 39C37.5523 39 38 38.5523 38 38C38 37.4477 37.5523 37 37 37C36.4477 37 36 37.4477 36 38C36 38.5523 36.4477 39 37 39Z"
                                stroke="#21B8C7" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                            <path d="M38 37L44 31M33 34L36 37L33 34Z" stroke="#21B8C7" stroke-width="2"
                                stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
    
                        <div class="mx-2">
                            <h3 class="text-2xl font-medium text-gray-800">6.8</h3>
                            <p class="mt-1 text-sm text-gray-500">Average mark</p>
                        </div>
                    </div>
                </div>

                <div class="flex items-center px-6 py-8 bg-white rounded-lg shadow-md shadow-gray-200 ">
                    <div class="flex items-center -mx-2">
                        <svg class="mx-2" width="70" height="70" viewBox="0 0 70 70" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="35" cy="35" r="35" fill="#FF4C61" fill-opacity="0.05" />
                            <path d="M26 32L32 38L36 34L43.405 41.405" stroke="#FF4C61" stroke-width="2"
                                stroke-linecap="square" />
                            <path d="M43.405 41.405L44 42" stroke="#FF4C61" stroke-width="2" stroke-linecap="round" />
                            <path d="M44 39V42H41" stroke="#FF4C61" stroke-width="2" stroke-linecap="square" />
                        </svg>
    
                        <div class="mx-2">
                            <h3 class="text-2xl font-medium text-gray-800">9 <span class="text-xl text-gray-600">(14%)</span></h3>
                            <p class="mt-1 text-sm text-gray-500">Underperforming students</p>
                        </div>
                    </div>
                </div>

                <div class="flex items-center px-6 py-8 bg-white rounded-lg shadow-md shadow-gray-200 ">
                    <div class="flex items-center -mx-2">
                        <svg class="mx-2" width="70" height="70" viewBox="0 0 70 70" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="35" cy="35" r="35" fill="#4CB8FF" fill-opacity="0.07" />
                            <path
                                d="M42 26V44H31C30.2044 44 29.4413 43.6839 28.8787 43.1213C28.3161 42.5587 28 41.7956 28 41V29C28 28.2044 28.3161 27.4413 28.8787 26.8787C29.4413 26.3161 30.2044 26 31 26H42Z"
                                stroke="#4CB8FF" stroke-width="2" stroke-linecap="square" />
                            <path d="M28 41C28 40.2044 28.3161 39.4413 28.8787 38.8787C29.4413 38.3161 30.2044 38 31 38H42"
                                stroke="#4CB8FF" stroke-width="2" stroke-linecap="square" />
                        </svg>
    
                        <div class="mx-2">
                            <h3 class="text-2xl font-medium text-gray-800">92%</h3>
                            <p class="mt-1 text-sm text-gray-500">Finished homeworks</p>
                        </div>
                    </div>
                </div>

                <div class="flex flex-col justify-center px-8 py-6 bg-white rounded-lg shadow-md shadow-gray-200 md:col-span-2 md:row-span-2 gap-y-4 gap-x-8 ">
                    <div class="sm:flex sm:items-center sm:justify-between">
                        <h2 class="font-medium text-gray-700">The number of applied and left students per month</h2>

                        <div class="flex items-center mt-4 -mx-2 sm:mt-0">
                            <span class="flex items-center text-gray-600">
                                <p class="mx-2">Applied</p>
                                
                                <span class="w-2 h-2 mx-2 bg-orange-500 rounded-full"></span>
                            </span>

                            <span class="flex items-center text-gray-600">
                                <p class="mx-2">Left</p>
                                <span class="w-2 h-2 mx-2 bg-indigo-500 rounded-full"></span>
                            </span>
                        </div>
                    </div>

                    <canvas class="max-w-3xl max-h-96" id="secondChart"></canvas>
                </div>

                <div class="row-span-3 bg-white rounded-lg shadow-md shadow-gray-200">
                    <div class="px-6 py-5 border-b border-gray-100 sm:flex sm:items-center sm:justify-between">
                        <h2 class="font-medium text-gray-700">Students by average mark</h2>

                        <button type="button" class="inline-flex focus:outline-none justify-center mt-2 text-sm font-medium leading-5 text-gray-500 bg-white rounded-lg sm:mt-0 hover:text-gray-600">
                            <span>Descending</span>
                            
                            <svg class="w-5 h-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                                <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                            </svg>
                        </button>
                    </div>
                    
                    <div class="p-6 space-y-6">
                        <div class="flex items-center justify-between ">
                            <div class="flex items-center">
                                <img class="w-10 h-10 overflow-hidden bg-gray-100 rounded-full object-cover" src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80">
                                <span class="mx-3 text-gray-600">Annette Watson</span>
                            </div>
                            <span class="font-semibold text-gray-600">9.3</span>
                        </div>

                        <div class="flex items-center justify-between ">
                            <div class="flex items-center">
                                <img class="w-10 h-10 overflow-hidden bg-gray-100 rounded-full object-cover" src="https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80">
                                <span class="mx-3 text-gray-600">Calvin Steward</span>
                            </div>
                            <span class="font-semibold text-gray-600">8.3</span>
                        </div>

                        <div class="flex items-center justify-between ">
                            <div class="flex items-center">
                                <img class="w-10 h-10 overflow-hidden bg-gray-100 rounded-full object-cover" src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80">
                                <span class="mx-3 text-gray-600">Ralph Richards</span>
                            </div>
                            <span class="font-semibold text-gray-600">8.9</span>
                        </div>

                        <div class="flex items-center justify-between ">
                            <div class="flex items-center">
                                <img class="w-10 h-10 overflow-hidden bg-gray-100 rounded-full object-cover" src="https://images.unsplash.com/photo-1599566150163-29194dcaad36?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80">
                                <span class="mx-3 text-gray-600">Bernard Murphy</span>
                            </div>
                            <span class="font-semibold text-gray-600">8.2</span>
                        </div>

                        <div class="flex items-center justify-between ">
                            <div class="flex items-center">
                                <img class="w-10 h-10 overflow-hidden bg-gray-100 rounded-full object-cover" src="https://images.unsplash.com/photo-1580489944761-15a19d654956?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=761&q=80">
                                <span class="mx-3 text-gray-600">Arlene Robertson</span>
                            </div>
                            <span class="font-semibold text-gray-600">7.8</span>
                        </div>

                        <div class="flex items-center justify-between ">
                            <div class="flex items-center">
                                <img class="w-10 h-10 overflow-hidden bg-gray-100 rounded-full object-cover" src="https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=764&q=80">
                                <span class="mx-3 text-gray-600">Jane Lane</span>
                            </div>
                            <span class="font-semibold text-gray-600">9.2</span>
                        </div>

                        <div class="flex items-center justify-between ">
                            <div class="flex items-center">
                                <img class="w-10 h-10 overflow-hidden bg-gray-100 rounded-full object-cover" src="https://images.unsplash.com/flagged/photo-1570612861542-284f4c12e75f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80">
                                <span class="mx-3 text-gray-600">Pat Mckinney</span>
                            </div>
                            <span class="font-semibold text-gray-600">6.9</span>
                        </div>

                        <div class="flex items-center justify-between ">
                            <div class="flex items-center">
                                <img class="w-10 h-10 overflow-hidden bg-gray-100 rounded-full object-cover" src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80">
                                <span class="mx-3 text-gray-600">Norman Walters</span>
                            </div>
                            <span class="font-semibold text-gray-600">9.9</span>
                        </div>
                    </div>
                </div>

                <div class=" bg-white rounded-lg shadow-md shadow-gray-200 lg:row-span-2">
                    <div class="px-6 py-5 border-b border-gray-100">
                        <h2 class="font-medium text-gray-700">Students by type of studying</h2>
                    </div>

                    <div class="flex items-center p-8">
                        <canvas class="max-w-sm" id="myChart"> </canvas>
                    </div>
                </div>

                <div class="flex items-center px-6 py-8 bg-white rounded-lg shadow-md shadow-gray-200 ">
                    <div class="flex items-center -mx-2">
                        <svg class="mx-2" width="70" height="70" viewBox="0 0 70 70" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="35" cy="35" r="35" fill="#FFB800" fill-opacity="0.07" />
                            <path d="M30 44H40M29 25H41V34C41 37.3137 38.3137 40 35 40C31.6863 40 29 37.3137 29 34V25Z"
                                stroke="#FFB800" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                            <path d="M35 40V44" stroke="#FFB800" stroke-width="2" stroke-linecap="round"
                                stroke-linejoin="round" />
                            <path
                                d="M29 28V34H28C26.3431 34 25 32.6569 25 31C25 29.3431 26.3431 28 28 28H29ZM41 34V28H42C43.6569 28 45 29.3431 45 31C45 32.6569 43.6569 34 42 34H41Z"
                                stroke="#FFB800" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
    
                        <div class="mx-2">
                            <h3 class="text-2xl font-medium text-gray-800">25</h3>
                            <p class="mt-1 text-sm text-gray-500">Lections left</p>
                        </div>
                    </div>
                </div>

                <div class="flex items-center px-6 py-8 bg-white rounded-lg shadow-md shadow-gray-200 ">
                    <div class="flex items-center -mx-2">
                        <svg class="mx-2" width="70" height="70" viewBox="0 0 70 70" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="35" cy="35" r="35" fill="#4CB8FF" fill-opacity="0.07" />
                            <path
                                d="M35 45C40.5228 45 45 40.5228 45 35C45 29.4772 40.5228 25 35 25C29.4772 25 25 29.4772 25 35C25 40.5228 29.4772 45 35 45Z"
                                stroke="#4CB8FF" stroke-width="2" stroke-linecap="square" />
                            <path d="M35 28V35L39 39" stroke="#4CB8FF" stroke-width="2" stroke-linecap="square" />
                        </svg>
    
                        <div class="mx-2">
                            <h3 class="text-2xl font-medium text-gray-800">139</h3>
                            <p class="mt-1 text-sm text-gray-500">Hours spent on lections</p>
                        </div>
                    </div>
                </div>
            </section>
        </main>
    </div>
</template>

<script>
import Chart from 'chart.js/auto';

export default {
    data() {
        return {
            isOpen: false,
            dropdownOpen: false
        }
    },

    mounted() {
        const charData = {
            type: 'doughnut',

            data: {
                labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple'],
                datasets: [{
                    label: '# of Votes',
                    data: [20, 20, 20, 10, 10],

                    backgroundColor: [
                        'rgba(153, 102, 255)',
                        'rgba(255, 206, 86)',
                        'rgba(255, 99, 132)',
                        'rgba(54, 162, 235)',
                        'rgba(75, 192, 192)',
                    ],
                    borderColor: [
                        'rgba(153, 102, 255, 1)',
                        'rgba(255, 206, 86, 1)',
                        'rgba(255, 99, 132, 1)',
                        'rgba(54, 162, 235, 1)',
                        'rgba(75, 192, 192, 1)',
                    ],
                }]
            },
            options: {
                plugins: {
                    legend: {
                        position: 'bottom',
                        fullSize: false,
                        align: 'start',
                        labels: {
                            padding: 10,
                            usePointStyle: true,
                            pointSytle: 'circle'
                        }
                    }
                },
            }
        };

        const data = [
            { x: 'Jan', applied: 19, left: 16 },
            { x: 'Feb', applied: 15, left: 8 },
            { x: 'Mar', applied: 24, left: 14 },
            { x: 'Apr', applied: 8, left: 7 },
            { x: 'May', applied: 11, left: 7 },
            { x: 'Jun', applied: 10, left: 6 },
            { x: 'Jul', applied: 17, left: 15 },
            { x: 'Aug', applied: 19, left: 18 },
            { x: 'Sep', applied: 18, left: 12 },
            { x: 'Oct', applied: 19, left: 20 },
            { x: 'Nov', applied: 18, left: 8 },
            { x: 'Dec', applied: 17, left: 12 },
        ];
        
        const secondcharData = {
            type: 'bar',
            data: {
                labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
                datasets: [{
                    label: 'Applied students',
                    borderRadius: 5,
                    data: data,
                    backgroundColor: '#FF7A00',
                    maxBarThickness: 5,
                    parsing: {
                        yAxisKey: 'applied'
                    },
                },
                {
                    label: 'Left students',
                    borderRadius: 5,
                    maxBarThickness: 5,
                    data: data,
                    backgroundColor: '#6F52ED',

                    parsing: {
                        yAxisKey: 'left'
                    },
                },

                ]
            },
            options: {
                responsive: true,


                scales: {
                    yAxes: [{
                        ticks: {
                            beginAtZero: true
                        }
                    }],
                    y: {
                        beginAtZero: true,
                        max: 25
                    },
                    x: {
                        grid: {
                            display: false
                        }
                    },
                },

                plugins: {
                    legend: {
                        display: false
                    }
                }
            }
        };

        const ctx = document.getElementById('myChart');
        const second = document.getElementById('secondChart');
        const myChart = new Chart(ctx, charData);
        const secondChart = new Chart(second, secondcharData);

        myChart;
        secondChart;
    }
}
</script>