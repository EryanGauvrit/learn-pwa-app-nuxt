<template>
    <main class="container max-w-4xl m-auto mt-10">
        <h1 class="text-4xl text-center mt-8 uppercase font-bold">Contact us</h1>
        <!-- Contact informations  -->

        <div class="flex flex-col gap-4">
            <h2 class="text-2xl font-bold text-center">Our contact informations</h2>
            <p>Phone: 123456789</p>
            <p>Email: test@example.com </p>
            <p>Address: 1234 Street, City, Country</p>
        </div>
        <!-- Add your form here -->

        <form class="flex flex-col justify-center gap-2 py-5">
            <Input label="Name" type="text" placeholder="Your name" />
            <Input label="Email" type="email" placeholder="Your email" />
            <Input label="Subject" type="text" placeholder="Subject" />
            <Input label="Message" type="text" placeholder="Your message" />

            <button type="submit" class="w-full bg-primary text-background py-2 rounded-md mt-10">Send</button>
        </form>
    </main>
</template>