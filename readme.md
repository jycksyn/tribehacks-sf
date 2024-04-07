# How to use this repository (Tribehacks Website)

## 1. Environment

Be sure you have NodeJS 18 installed. You can install it from [here](https://nodejs.org/en/download). 

## 2. Packages

Clone the repository. Then, run `npm i` (or use `pnpm` to save disk space) to install the dependencies.

## 3. Environment Variables

Make a copy of `env.txt` and rename it to `.env`.

## 4. Start Development server

To start the website in local development mode so that it will auto-refresh. It will give you an IP address where you can access the website.

```bash
npm run dev
```

Also, in a new terminal window, run this script to activate the CMS backend. This allows you to change page content without editing the code.

```bash
npm run cms-proxy-server
```

Once both of these are running, you can access the CMS at `http://<IP-ADDRESS-GIVEN>/admin`.

---

## How to edit the code of blocks:

In order to make changes to blocks so editors can access them in the CMS, make sure to follow these instructions.

1. In the `cms/` folder, modify the features in presumably `common.js`. You can copy an existing feature within the block.

2. Modify the [Zod](https://zod.dev/) schema in config.ts to include the new property.

3. Edit the code of the block in `components/Block`