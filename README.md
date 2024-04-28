# brock
brock


module decoder(a,en,y);
input [2:0]a;
input en;
outputreg [7:0]y;
always @(a or en)
begin

if(en)
y=1'b11111111;
else
case(a)
3'b000:y=8'b01111111;
3'b001:y=8'b10111111;
3'b010:y=8'b11011111;
3'b011:y=8'b11101111;
3'b100:y=8'b11110111;
3'b101:y=8'b11111011;
3'b110:y=8'b11111101;
3'b111:y=8'b11111110;
endcase
end
endmodule
