# Token Address and Verified Code

https://testnet.bscscan.com/address/0x4c4358DA60Ca1deb81614Ffa128bF722d1fa27bD#code

# Presale Address and Verified Code

https://testnet.bscscan.com/address/0x228c22518f4f9b106f1c53399eb563ec30d161f1#code

.env requires API_key for verifying as well as MNEMONIC for deploying

cd client
npm install or yarn
npm start or yarn start

Only contract deployer can view admin panel and create a new presale round!

client/src/App.js

              <Route
                path="/mint"
                element={
                  Boolean(userCtx.appOwner === web3Ctx.account) ? (
                    <MintPeriod />
                  ) : (
                    <NotFound />
                  )
                }
              />

              <Route
                path="/admin"
                element={
                  Boolean(userCtx.appOwner === web3Ctx.account) ? (
                    <Admin />
                  ) : (
                    <NotFound />
                  )
                }
              />

change '<NotFound />' to the same as the option to it's left to display AppOwner areas during local usage
you will not be able to interact with the contracts like the admin would so I advise just redeploying!
