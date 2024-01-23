<footer class="py-20 sm:py-32 bg-black border-t border-solid border-green-700 flex flex-col gap-4 sm:gap-8 justify-center items-center">
    <div class="flex-[0.75] bg-green-500 p-12 rounded-2xl">
        <h3 class="font-bold font-poppins text-4xl sm:text-5xl md:text-6xl">Connect with me</h3>
        <form id="connect" class="mt-10 flex flex-col gap-6 font-poppins">
            <label class="flex flex-col">
                <span class="font-bold mb-4">Name</span>
                <input type="text" name="name" placeholder="What's your name?" class="py-4 px-6 placeholder:text-taupe text-black bg-white rounded-lg font-medium border-2 border-green-500 focus:outline-none focus:border-darkGreen focus:ring focus:ring-darkGreen" value>
            </label>
            <label class="flex flex-col">
                <span class="text-dim font-bold mb-4">Email</span>
                <input type="email" name="email" placeholder="What's your email?" class="py-4 px-6 placeholder:text-taupe text-black bg-white rounded-lg font-medium border-2 border-green-500 focus:outline-none focus:border-darkGreen focus:ring focus:ring-darkGreen" value>
            </label>
            <label class="flex flex-col">
                <span class="text-dim font-bold mb-4">Message</span>
                <textarea id="messageInput" name="message" placeholder="What's your message?" class="py-4 px-6 placeholder:text-taupe text-black bg-white rounded-lg font-medium border-2 border-green-500 focus:outline-none focus:border-darkGreen focus:ring focus:ring-darkGreen"></textarea>
            </label>
            <button type="button" onclick="sendEmail()" class="mx-auto px-4 py-2 rounded-md border border-solid border-green flex -mb-6 sm:-mb-0 -mt-0 transition duration-200 transform hover:text-darkGreen hover:scale-105">
                <p class="font-family: poppins; font-size: inherit; display: inline-block; vertical-align: middle;"><strong>Send</strong></p>    
            </button>                             
        </form>
        <script>
            function sendEmail() {
                var messageInputValue = document.getElementById('messageInput').value;
                var mailtoLink = 'mailto:nckmingace@gmail.com?subject=Inquiry&body=' + encodeURIComponent(messageInputValue);
                window.location.href = mailtoLink;
            }
        </script>
    </div>
    <div class="mt-14 text-sm"> Copyright &copy; 2024 Nicholas Mingace | All Rights Reserved.</div>
</footer>