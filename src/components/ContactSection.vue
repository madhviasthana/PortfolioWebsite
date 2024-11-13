<template>
    <section class="text-white mt-20" id="contact">
        <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Let's Connect</h2>
        <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
            <!-- Contact Info Section -->
            <div>
                <p class="text-[#adb7be]">
                    I would love to hear from you! Whether you have a question about a project, collaboration, or just want to say hi, feel free to reach out.
                </p>
                <div class="col-lg-4 col-md-4 mb-lg-0 mt-5">
                    <!-- Email -->
                    <div class="flex mb-10 items-center">
                        <div class="p-2"
                            style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                        overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                            <img src="https://img.icons8.com/metro/50/ffffff/new-post.png" alt="new-post" class="w-6">
                        </div>
                        <div class="ml-5 text-white">
                            <h4>Email</h4>
                            <p>madhviasthana9@gmail.com</p>
                        </div>
                    </div>
                    <!-- Phone -->
                    <div class="flex mb-10 items-center">
                        <div class="p-2"
                            style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                        overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                            <img src="https://img.icons8.com/ios-filled/50/ffffff/phone.png" alt="phone" class="w-6">
                        </div>
                        <div class="ml-5 text-white">
                            <h4>Phone</h4>
                            <p>+49 15730252898</p>
                        </div>
                    </div>
                    <!-- LinkedIn -->
                    <div class="flex mb-10 items-center">
                        <div class="p-2"
                            style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                        overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                            <img src="https://img.icons8.com/ios-filled/50/ffffff/linkedin.png" alt="linkedin"
                                class="w-6">
                        </div>
                        <div class="ml-5 text-white">
                            <h4>LinkedIn</h4>
                            <p><a href="https://www.linkedin.com/in/madhviasthana/" target="_blank" class="hover:underline">
                                https://www.linkedin.com/in/madhviasthana/
                            </a></p>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Contact Form Section -->
            <div
                style="background: #111a3e; width: 100%;height: 100%; border-radius: 20px;
                overflow: hidden;border: 1px solid #111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                <form class="flex flex-col p-6" data-aos="zoom-in-up">
                    <div class="mb-6">
                        <label for="email" class="text-white block mb-2 text-sm font-medium">Email</label>
                        <input type="email" id="email" class="bg-[#111827] placeholder-[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                            placeholder="email@gmail.com" name="email">
                    </div>
                    <div class="mb-6">
                        <label for="subject" class="text-white block mb-2 text-sm font-medium">Subject</label>
                        <input type="text" id="subject" class="bg-[#111827] placeholder-[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                            placeholder="Your subject here" name="subject">
                    </div>
                    <div class="mb-6">
                        <label for="message" class="text-white block mb-2 text-sm font-medium">Message</label>
                        <textarea id="message" class="bg-[#111827] placeholder-[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                            placeholder="Write your message..." name="message"></textarea>
                    </div>
                    <button type="submit" class="z-1 px-6 py-3 rounded-full text-white bg-primary hover:bg-opacity-90 border-2 border-transparent">
                        Send Message
                    </button>
                </form>
            </div>
            <!-- Decorative Gradient -->
            <div class="bg-gradient-to-tr opacity-25 from-[#570cac] to-primary blur-2xl h-20 w-80 z-0 absolute -top-1/2 -left-4 transform -translate-x-2/3 
            -translate-1/2">
            </div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'ContactSection',
};
</script>
