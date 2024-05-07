<template>
    <main class="container max-w-4xl m-auto mt-10">
        <h1 class="text-2xl">Contact us</h1>
        <!-- Contact informations  -->

        <div class="flex flex-col gap-4">
            <h2 class="text-xl">Our contact informations</h2>
            <p>Phone: 123456789</p>
            <p>Email: test@example.com </p>
            <p>Address: 1234 Street, City, Country</p>
        </div>
        <!-- Add your form here -->

        <form class="flex flex-col justify-center">
            <div class="grid grid-cols-3">
                <label for="name">Name</label>
                <input type="text" id="name" name="name" required>
            </div>
            <label for="name">Name</label>
            <input type="text" id="name" name="name" required>

            <label for="email">Email</label>
            <input type="email" id="email" name="email" required>

            <label for="message">Message</label>
            <textarea id="message" name="message" required></textarea>

            <button type="submit">Send</button>
        </form>
    </main>
</template>